---
layout: page
title: About CoyIM
permalink: /about-coyim/
---

CoyIM is a standalone chat client with a focus on safety and security. It is a self contained program that runs on Windows, Linux and OS X. CoyIM only supports one chat protocol - XMPP (which is sometimes known as Jabber). The goal of CoyIM is not to have every feature under the sun. Instead we want to carefully pick and choose the features that are necessary to create a good chat experience, while keeping the attack surface of the system to a minimum.

In addition to choosing features carefully, we have also built in support for Tor, OTR and TLS. The Tor support allows users to become anonymous when chatting. OTR makes end-to-end encryption of communication possible. And TLS adds another layer of encryption to the communication with the chat servers. We have built these features to be core parts of the application - they are not plugins or extras in any way.

CoyIM is implemented in Golang. We made this choice to make it easier to protect our users. Many other implementation languages open up the door for a large number of attacks. We try to minimize those risks by using Golang.

Finally, we want CoyIM to be safe from the moment you start it up. We want it to be possible to just start using the application and everything will be done the right way. In some cases you can turn off the safe defaults, but you will not have to configure anything extra to get all the protection we can give you.

How to Use
===

CoyIM have lots of features that exist in most other chat clients as well - however, there are some things we do differently that most other clients don't do. These are some of the features that set us apart:

* CoyIM has support for the latest version of OTR (a protocol for doing encrypted chat) built in at the core
* CoyIM will automatically detect Tor if it is installed and use it to connect
* It will also automatically use a Tor Onion Service if one is known for the server in question
* It will also use separate Tor circuits for each account, in order to make it harder to tie the accounts together
* If more than one account is configured, when connecting CoyIM will insert random delays before connecting to each account, in order to make fingerprinting of connections between accounts harder
* If Tor is available, CoyIM will do the SRV lookup for the server over Tor
* CoyIM can import both account settings, OTR settings, fingerprints and private keys from other clients such as Pidgin, Adium, Gajim and xmpp-client
* CoyIM can save all your configuration, including OTR fingerprints and keys, in an encrypted configuration file.

