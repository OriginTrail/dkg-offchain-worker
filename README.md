<!-- markdown-link-check-disable -->
# DKG Offchain Worker Module

The DKG Offchain Worker: A simple offchain worker demonstrating 
how to fetch data from OriginTrail Decentralized Knowledge Graph

We are providing here substrate template node with integrated DKG Offchain Worker
so you can start hacking right away. DKG-ocw is after a new block is produced, 
running trail command on DKG network about predefined dataset that is already imported to the network.

## Getting Started

Follow the steps below to get started with the Node Template and DKG Offchain Worker.

### Start local DKG network

To start local DKG network on your machine you should follow instructions on this [link](https://docs.origintrail.io/developers/setting-up-development-environment)

After you go through instructions, then you need to publish data to DKG, our recommendation is to publish `~/ot-node/importers/json_examples/local-query1.json`. You can publish it using [instructions](https://docs.origintrail.io/developers/devsinstall)(usinga nodejs dkg client ) or using postman (inside ~/ot-node/postman there is postman collection that can be imported and used).

### Rust Setup

First, complete the [basic Rust setup instructions](./docs/rust-setup.md).

### Run

Use Rust's native `cargo` command to build and launch the template node:

```sh
cargo run --release -- --dev --tmp
```

### Build

The `cargo run` command will perform an initial build. Use the following command to build the node
without launching it:

```sh
cargo build --release
```

If you have some issues with building, run `cargo clean` and after that again `cargo build`.

## Run

The provided `cargo run` command will launch a temporary node and its state will be discarded after
you terminate the process. After the project has been built, there are other ways to launch the
node.

## Learn More

- More about [OriginTrail](https://origintrail.io/)
- More about [decentralized knowledge graph](https://origintrail.io/technology)
- Video explainer about [the world’s first Decentralized Knowledge Graph](https://www.youtube.com/watch?v=AsCUigu39Hw&ab_channel=OriginTrail)
- More about expanding the multi-chain OriginTrail with Polkadot you can find on 
  [parachain.origintrail.io](https://parachain.origintrail.io/)
- Refer to the upstream
[Substrate Developer Hub Node Template](https://github.com/substrate-developer-hub/substrate-node-template)
to learn more about the structure of this project, the capabilities it encapsulates and the way in
which those capabilities are implemented.