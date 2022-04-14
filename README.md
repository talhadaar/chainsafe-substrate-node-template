# Gossamer Test Node

This repository contains a [FRAME runtime](https://docs.substrate.io/v3/runtime/frame/) that is designed for testing the
[Gossamer](https://github.com/ChainSafe/gossamer) implementation of the
[Polkadot Host](https://wiki.polkadot.network/docs/glossary#polkadot-host). In addition to the runtime, this repository
contains a Substrate client that can be used to host the runtime and participate in a blockchain network, as well as
generate chain specification files.

This repository was forked from the
[Substrate Node Template](https://github.com/substrate-developer-hub/substrate-node-template); the following changes
have been made to the runtime:

- The [Aura](https://docs.substrate.io/v3/getting-started/glossary/#authority-round-aura) block authorship mechanism has
  been replaced with
  [BABE](https://docs.substrate.io/v3/getting-started/glossary/#blind-assignment-of-blockchain-extension-babe), which
  means the [Aura pallet](https://crates.parity.io/pallet_aura/index.html) has been removed, and the
  [BABE](https://crates.parity.io/pallet_babe/index.html) and
  [Authorship](https://crates.parity.io/pallet_authorship/index.html) pallets have been added.
- The [Randomness Collective Flip](https://crates.parity.io/pallet_randomness_collective_flip/index.html) and
  [Template](https://crates.parity.io/pallet_template/index.html) pallets have been removed.
