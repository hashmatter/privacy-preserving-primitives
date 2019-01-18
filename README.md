# Privacy preserving primitives

This repo lists implementations, design and papers of primitives and 
protocols aiming at increasing privacy of networked systems. The goal of this
project is to create the go-to directory for developers and system designers to
learn about the existing tools for developing applications which are privacy
preserving.

## Index

**A. Data structures**
- [ClaimChain](https://github.com/hashmatter/privacy-preserving-primitives/#claimchain)

**B. Secure messaging**
- [Sphinx](https://github.com/hashmatter/privacy-preserving-primitives/#sphinx)
- [HORNET](https://github.com/hashmatter/privacy-preserving-primitives/#hornet)

## A. Data structures

### ClaimChain

[ClaimChain](https://claimchain.github.io/) is a cryptographic primitive
providing a privacy-preserving, authenticated and decentralized data store of
claims. The [paper](https://arxiv.org/abs/1707.06279) shows how to use 
ClaimChain as a privacy-preserving decentralized public key distribution.

*when to use it*: In P2P or centralized systems in which clients and/or servers
need to edit and share verifiable and authenticated data structures with 
fine-grained access control. This primitive does not require a central point of
authority to provide its properties, although it does not provide consensus out
of the box (i.e. there is no mechanism to ensure all users have the same version
of the ClaimChain at the same point).

- **website**: [ClaimChain](https://claimchain.github.io/)
- **research**: [original paper](https://arxiv.org/abs/1707.06279)
- **implementations**: [Python](https://github.com/claimchain/claimchain-core)
- **tags**: data-structure, merkle-tree, p2p, PKI.


## B. Secure messaging

### Sphinx

[Sphinx](https://katzenpost.mixnetworks.org/docs/specs/sphinx.html) is a compact
cryptographic packet format that can be used in onion routing, mix networks and
as a general purpose secure transport between senders and intermediate relays in
P2P networks. Sphinx uses Diffie Hellman to derive the shared keys between the 
sender of the message and the relayers. Designers and developers can chose the
family of cryptographic primitives to use, depending on the cases.

*when to use it*: In network applications in which relay nodes should not learn
anything about the source, destination and content of the message to relay,
besides the information needed to forward the message to the next hop.

- **research**: [original paper](https://cypherpunks.ca/~iang/pubs/Sphinx_Oakland09.pdf)
- **implementations**: [rust-sphinxcrypto](https://github.com/applied-mixnetworks/rust-sphinxcrypto), [lightning-onion (Golang)](https://github.com/lightningnetwork/lightning-onion)
- **tags**: mix-networks, onion-routing, anonymous-communication.

### HORNET

[HORNET](https://netsec.ethz.ch/research/anonymity.php) is a high-speed
anonymous communication protocol designed to be deployed at a network level by
Future Internet Architectures by default. The message relays do not keep state 
of anonymous communications. Instead, the state of the anonymous channel is
included in the message itself.

*when to use it*: On top of P2P overlay networks (e.g. DHTs) to provide protection
against packet/message correlation, session linkage, metadata leaks and to
protect against passive network adversaries. Any P2P messaging application which
uses multiple message relays can use HORNET to provide metadata protection
against passive and global adversaries.


- **website**: [HORNET](https://netsec.ethz.ch/research/anonymity.php)
- **research**: [original  paper](https://netsec.ethz.ch/publications/papers/chen_hornet_ccs15.pdf)
- **implementations**: [Golang](https://github.com/hashmatter/hornet)
- **tags**: onion-routing, anonymous-communication, protocol.

---

# Community

Join our community of developers and researchers working on privacy preserving
networks and applications at the [gitter channel](https://hashmatter.com).

## Contributing
Check the issues for ideas on how to help the project. When adding a new project
to the list, use the same item structure. Fork and PR for adding or improve content.

## License

© MIT
hashmatter (https://hashmatter.com)
