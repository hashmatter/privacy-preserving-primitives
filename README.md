# Privacy preserving primitives

This repo lists project implementations, designs and papers of primitives and 
protocols aiming at increasing privacy of networked systems. The goal of this
project is to create the go-to directory for developers and system designers to
learn about the existing tools for developing applications which are privacy
preserving.

## Data structures

### ClaimChain

[**ClaimChain**](https://claimchain.github.io/) is a cryptographic primitive
providing a privacy-preserving, authenticated and decentralized data store of
claims. The [paper](https://arxiv.org/abs/1707.06279) shows how to use 
ClaimChain as a privacy-preserving decentralized public key distribution.

*when to use it*: In P2P or centralized systems in which clients and/or servers
need to edit and share verifiable and authenticated data structures with 
fine-grained access control. This primitive does not require a central point of
authority to provide its properties, although it does not provide consensus out
of the box (i.e. there is no mechanism to ensure all users have the same version
of the ClaimChain at the same point).

- **website**: [**Claimchain**](https://claimchain.github.io/)
- **research**: [original paper](https://arxiv.org/abs/1707.06279)
- **implementations**: [Python](https://github.com/claimchain/claimchain-core)
- **tags**: data-structure, merkle-tree, p2p, PKI.

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
