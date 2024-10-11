# Create a Parachain from scratch

The repository contains two nodes `parachain-node` and `solochain-node` and one `runtime`. The goal of this tutorial is to help you convert your Substrate runtime to be compatible with the `parachain-node` and register a new parachain on the PASEO testnet. 

About additional resources, you could learn more about the Parachain network architecture in here: 
- Breakdown the sharded network design of Polkadot: https://x.com/chungquantin/status/1809864276850704882
- Breakdown Relaychain hybrid consensus: https://x.com/openguildwtf/status/1809203505649037391

## Getting started
First step is to follow all the TODOs in the repository and convert your `solochain-runtime` to a `parachain-runtime` until it works with the `parachain-node`. To test the the local relaychain network, run the below command:
```
pop up parachain -f ./network.toml
```

If you are not familiar with the `pop-cli` tool, learn more in here: https://github.com/r0gue-io/pop-cli

### Convert a solochain node to a parachain node with Cumulus
### Resolve all the TODOs
![image](https://github.com/user-attachments/assets/d6ec39a0-ff1f-47b9-8a79-30c12bb4dec4)

### Materials to learn about Cumulus
- Polkadot SDK - Cumulus: [https://github.com/paritytech/polkadot-sdk/tree/master/cumulus](https://github.com/paritytech/polkadot-sdk/tree/master/cumulus)
- Polkadot SDK Guide - Cumulus: [https://paritytech.github.io/polkadot-sdk/master/polkadot_sdk_docs/polkadot_sdk/cumulus/index.html](https://paritytech.github.io/polkadot-sdk/master/polkadot_sdk_docs/polkadot_sdk/cumulus/index.html)
- Runtime modules & configuration:
  - cumulus_pallet_parachain_system: [https://paritytech.github.io/polkadot-sdk/master/cumulus_pallet_parachain_system/index.html](https://paritytech.github.io/polkadot-sdk/master/cumulus_pallet_parachain_system/index.html)
  - staging_parachain_info: [https://paritytech.github.io/polkadot-sdk/master/staging_parachain_info/index.html](https://paritytech.github.io/polkadot-sdk/master/staging_parachain_info/index.html)
	- register_validate_block: [https://paritytech.github.io/polkadot-sdk/master/cumulus_pallet_parachain_system/macro.register_validate_block.html](https://paritytech.github.io/polkadot-sdk/master/cumulus_pallet_parachain_system/macro.register_validate_block.html)

### Register a parachain on the testnet relaychain
- Obtain a unique identifier for your parachain
- Register a parachain
  - Reserve a **unique identifier** on the specific relay chain that you want to connect to.
	- Compile the WebAssembly runtime binary
	- Generate the genesis state from the chain specification for the parachain.
- Obtain a parachain slot (No longer valid due to **Polkadot 2.0 - Agile Coretime**)
- Acquire a parachain execution core on Coretime Marketplace [https://app.regionx.tech/?network=paseo](https://app.regionx.tech/?network=paseo)
  - Go to **PASEO faucet** to request some testnet tokens: [https://faucet.polkadot.io/](https://faucet.polkadot.io/)
	- Transfer from **PASEO Relaychain** to **PASEO Coretime**
	- Purchase a new core on **PASEO network**
	- Check a new core: [https://app.regionx.tech/regions?network=paseo&paraId=2034&core=24](https://app.regionx.tech/regions?network=paseo&paraId=2034&core=24)
- Open Message Passing Channels
- Deploy a reversed parachain to an execution core
