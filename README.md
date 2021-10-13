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


## What is a Decentralized Knowledge Graph (DKG)


There are many avaialable definitions of a knowlege graph, therefore we will present a simplified one focused on usability, rather than completeness. The purpose of this introduction is not to be a comprehensive guide for knowledge graphs, however it aims to get you started with the basics.

A **knowledge graph (KG)** is a network of entities — physical & digital objects, events or concepts — illustrating the relationship between them (aka a semantic network). KGs are used by major companies such as [Amazon](http://lunadong.com/talks/PG.pdf), [Google](https://en.wikipedia.org/wiki/Google_Knowledge_Graph), [Uber](https://www.youtube.com/watch?v=r3yMSl5NB_Q), [IBM](https://www.ibm.com/cloud/learn/knowledge-graph) etc for various applications: search, data integration, knowledge reasoning, recommendation engines, analytics, machine learning and AI etc.

Key characteristics of knowledge graphs:
* focus on data connections as "first class citizens" (linked data) 
* designed to ingest data from multiple sources, usually in different formats
* flexible data model, easily extendable

Common knowledge graphs however are deployed within the domain of one organization and are designed to capture knowledge from various sources both from within and outside of the organization.

We define **decentralized knowledge graph (DKG)** as a global shared knowledge graph that is designed to benefit organizations and individuals by providing a common infrastructure for data exchange. The DKG:

* Enables Dapps with search, integration, analytics, AI and ML capabilities for any data source: blockchains, IPFS, enterprise systems, web services, personal devices 
* Removes central authorities (decentralized infrastructure)
* Enables permissionless PUBLISH and QUERY (public network)
* Decentralized identity & Verifiable Credentials based access control (references private data)

## The OriginTrail DKG Architecture 

The OriginTrail Decentralized Network implements the DKG according the the OriginTrail protocol.

It is:

* **a permissionless network** - anyone can run OriginTrail nodes
* **a multi-chain data exchange network** - connects to several blockchains (currently Ethereum and xDai with more integrations upcoming such as with Polkadot)
* **designed for off-chain data exchange using standardized data models** (GS1 & W3C standards and recommendations)
* **public open source software**
* **infrastructure for knowledge marketplaces & tenders** - more info [here](https://www.youtube.com/watch?v=4uCxYGRh5fk)

More information is available on the OriginTrail [website](https://origintrail.io), [official documentation](https://docs.origintrail.io) and [blog](https://medium.com/origintrail).


![](https://i.imgur.com/yTNtZE1.png)

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