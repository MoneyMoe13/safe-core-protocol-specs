# Objective

In order for Ethereum to succeed there needs to be a (transition)[https://vitalik.ca/general/2023/06/09/three_transitions.html] of user accounts to smart-contract based accounts (“smart accounts”). This transition is enabled through account abstraction and supported by efforts like [ERC-4337](https://eips.ethereum.org/EIPS/eip-4337), [ERC-6900](https://eips.ethereum.org/EIPS/eip-6900), and others. However, there are some challenges that have to be addressed in order to ensure the success of the smart account ecosystem.

- **Portability:** Current user-accounts (EOAs) are a widely accepted standard allowing accounts to be portable across wallets and applications. Smart accounts may create vendor lock-in due to wallets creating their proprietary smart accounts which is a step back from current fully portable EOA accounts.
- **Composability:** With multiple teams building smart accounts, tooling, standards and applications may have to choose which one(s) to be compatible with. This may result in a major fragmentation of the Ethereum ecosystem.
- **Security:** Smart accounts may introduce smart-contract bugs and other vulnerabilities, similar to other smart-contract based systems like bridges or DeFi protocols.

In order to address those, the Safe{Core} Protocol proposes an open framework for modular smart accounts that are portable, composable and secure. The protocol is inspired by the learnings from the Safe Smart Account, but is fundamentally account-agnostic. It aims to achieve maximum reuse of components in order to establish strong security guarantees.


The objective of the protocol is to `enforce` a set of `rules` within the `smart account ecosystem`.


- What `rules` does the protocol enforce?
    - Support specific contract interfaces of the Safe{Core} Protocol Specs
    - Comply with requirements defined in the Registry
- How are these rules `enforced`?
    - Inclusion criteria for the Registry
    - Examples
        - App store (listing requirements)
        - Https
- What is the `smart account ecosystem`?
    - Contracts: Plugins, Hooks, Signature Verifiers, Function Handlers
    - Infrastructure: Indexers, Relayers, …
    - Interfaces: Web Interfaces, dApps, …


This initial version of Safe{Core} Protocol has a strong focus on onchain components (accounts, integrations). In the long run, the protocol should also cover offchain components (indexers, user interfaces). 
