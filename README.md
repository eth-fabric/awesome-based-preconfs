# Awesome Preconfirmations [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of resources, research, and implementations related to preconfirmations in the Ethereum ecosystem.

## Table of Contents
- [Introduction](#introduction)
- [Research and Discussion](#research-and-discussion)
- [Talks](#talks)
- [Implementations](#implementations)
- [Based Rollup](#based-rollups)
- [Related Concepts](#related-concepts)
- [Contributing](#contributing)

## Introduction
Preconfirmations are a mechanism that allows block proposers to commit to a block's contents before it is included in the blockchain. Follow the Ethereum Sequencing and Preconfirmations calls [here](https://www.youtube.com/watch?v=jrm4ZUoj9xY&list=PLJqWcTqh_zKHDFarAcF29QfdMlUpReZrR).

## Research and Discussion
- [Based Preconfirmations](https://ethresear.ch/t/based-preconfirmations/17353) - The original post introduces the concept of based preconfirmations.
- [Strawmanning Based Preconfirmations](https://ethresear.ch/t/strawmanning-based-preconfirmations/19695) - Analysis of a simple “strawman” preconfirmation setup.
- [Value-Capturing Based Rollups with Preconfirmations](https://collective.flashbots.net/t/value-capturing-based-rollups-with-based-preconfirmations) - A protocol which allows for based rollups to capture value generated from block building with preconfirmations.
- [Leaderless and Leader-Based Preconfirmations](https://ethresear.ch/t/leaderless-and-leader-based-preconfirmations) - Discussion on leader-based and leaderless preconfs.
- [Analyzing BFT & Proposer-Promised Preconfirmations](https://ethresear.ch/t/analyzing-bft-proposer-promised-preconfirmations/17963) - Analysis of BFT preconfirmations and proposer-promised preconfirmations.
- [Rollup-Centric Considerations of Based Preconfimations](https://ethresear.ch/t/rollup-centric-considerations-of-based-preconfimations)- Explores how implementations of preconfirmations can configure blocktime and more efficient data publishing
- [Integrating Account Abstraction and Inclusion Preconfirmations](https://research.chainbound.io/integrating-account-abstraction-and-inclusion-preconfirmations) - Proposal to directly leverage EIP-7702 for adoption of preconfs benefiting from batching, gas sponsorship, and secure delegations.
- [Preconfirmation for the Average Joe](https://x.com/ceciliaz030/status/1875558701324759392) - Simple explnation on preconfs.
- [Preconfirmations for Vanilla Based Rollups](https://github.com/LimeChain/based-preconfirmations-research/blob/732cb92474554c2529aabc61e83b8f0934ce6adf/docs/preconfirmations-for-vanilla-based-rollups.md) - Document outlines the design and mechanics to support preconfirmations in Vanilla Based Rollups.
  
## Fair Exchange
- [Preconfirmation Fair Exchange](https://ethresear.ch/t/preconfirmation-fair-exchange/21891) - Framework for analyzing protocols that seek to enforce timely-fair exchange of preconfirmations.
- [Solutions to the Preconf Fair Exchange Problem](https://ethresear.ch/t/solutions-to-the-preconf-fair-exchange-problem/19779) - Solutions for dealing with the fair exchange problem in leader-based preconfirmation setups.


## Sidecars
- [A simple, small, mev-boost compatible preconfirmation idea](https://ethresear.ch/t/a-simple-small-mev-boost-compatible-preconfirmation-idea/19800) - Adjusting MEV-Boost to handle preconfs.
- [Based Preconfirmations with Multi-round MEV-Boost](Based Preconfirmations with Multi-round MEV-Boost) - Propose multi-round MEV-Boost, a modification of MEV-Boost that enables based preconfirmations by running multiple rounds of MEV-Boost auctions within a single slot.
- [Commit-Boost: Proposer Platform to Safely Make Commitments](https://ethresear.ch/t/commit-boost-proposer-platform-to-safely-make-commitments/20107) - New sidecar that allows proposers to make commitments to preconf protocols.
- [Based proposer commitments - Ethereum’s marketplace for proposer commitments](https://ethresear.ch/t/based-proposer-commitments-ethereum-s-marketplace-for-proposer-commitments) - New sidecar that allows proposers to make commitments to preconf protocols.
- [Block Building Pipelines for Vanilla Based Rollups](https://github.com/LimeChain/based-preconfirmations-research/blob/732cb92474554c2529aabc61e83b8f0934ce6adf/docs/pipelines.md)

## Validators
[Delegation in Bolt: Outsourcing Sophistication While Preserving Decentralization](https://research.chainbound.io/delegation-in-bolt-outsourcing-sophistication-while-preserving-decentralization) - Article explores various “levels” of delegation from proposers for preconfs. 
[Preconfirmations under the NO lens](https://ethresear.ch/t/preconfirmations-under-the-no-lens/19975) - Research analyzing preconfs from a validator's perspective. 

## Universal Registry for Commitments
- [Credibly Neutral Preconfirmation Collateral: The Preconfirmation Registry](https://ethresear.ch/t/credibly-neutral-preconfirmation-collateral-the-preconfirmation-registry/19634) - Introduces a design for a credibly neutral preconfirmations registry.
- [Based Sequencer Selection](https://ethresear.ch/t/based-sequencer-selection/19747) - Exploratory proposal for a method of deterministically identifying sequencers on L2s to route transactions to.
- [Sequencer Opt-In, Discovery and Communication](https://github.com/LimeChain/based-preconfirmations-research/blob/732cb92474554c2529aabc61e83b8f0934ce6adf/docs/optin-mechanics.md) - Inital exploration for validators to register / opt in to based sequecning.
- [Universial Registry Contract](https://github.com/eth-fabric/urc) - Developed by over a dozen teams and currently being used by multiple preconf teams. Documents can be found in the Github.

## Pricing and Incentive Mechanisms
- [Avoiding Accidental Liveness Faults for Based Preconfs](https://ethresear.ch/t/avoiding-accidental-liveness-faults-for-based-preconfs) - Proposal to solve accidental liveness slashing for proposers offering preconfs.
- [User-Defined Penalties: Ensuring Honest Preconf Behavior](https://ethresear.ch/t/user-defined-penalties-ensuring-honest-preconf-behavior/19545) - Post outlining how users should specify their preferred penalty when requesting a preconf.
- [Pre-confirmation Liveness Slashing Penalties from the Proposer’s Perspective](https://ethresear.ch/t/pre-confirmation-liveness-slashing-penalties-from-the-proposers-perspective/19884) - Explores the liveness penalty from the point of view of proposers from an economical perspective.
- [Pricing Transactions for Preconfirmation](https://ethresear.ch/t/pricing-transactions-for-preconfirmation/21802) - Proposes a framework for pricing preconfirmations but also to initiate a constructive discussion within the Ethereum community.
- [Pricing Ethereum Blocks with Vol Markets with Implications for Preconfirmations](https://ethresear.ch/t/pricing-ethereum-blocks-with-vol-markets-with-implications-for-preconfirmations/20419) - A discussion and illustrate approach for the pricing of preconfs that responds in real-time to current market conditions.
- [Estimating the Revenue from Independent Sub-Slot Auction Preconfirmations](https://research.lido.fi/t/estimating-the-revenue-from-independent-sub-slot-auction-preconfirmations/8801) - Analysis towards understanding the economic feasibility of preconfirmations.
- [A Pricing Model for Inclusion Preconfirmations](https://research.lido.fi/t/a-pricing-model-for-inclusion-preconfirmations/9136) - Article focuses on the pricing of inclusion preconfirmations.
- [Pricing Future Blockspace: A Data-driven Approach](https://www.luban.wtf/taiyi-pricing-1) - Introduce a pricing model developed for hedged preconfirmations with a focus on preserving underwriter funds and generating steady yields.
- [Analysing Expected Proposer Revenue from Preconfirmations](https://research.lido.fi/t/analysing-expected-proposer-revenue-from-preconfirmations/8954) - Article exploring expected revenue from preconfirmations vs the current MEV-Boost acution.

## Gateways and Delegation
- [Ahead-of-Time Block Auctions To Enable Execution Preconfirmations](https://ethresear.ch/t/ahead-of-time-block-auctions-to-enable-execution-preconfirmations/21345) - Article analyzing a gateway as an unsophisticated entity and the other as a sophisticated builder.

## Stacks / Implmentations
- [Bolt](https://chainbound.github.io/bolt-docs/) - Bolt enables Ethereum block proposers to provide credible commitments about the contents of their blocks.
- [Espresso](https://docs.espressosys.com/sequencer) - Espresso allows applications to sell their sequencing rights through an open marketplace. 
- [mev-commit](https://docs.primev.xyz/) - A credible commitment network used for preconfirmations & more.
- [Preconfirmations: On splitting the block, mev-boost compatibility and relays](https://ethresear.ch/t/preconfirmations-on-splitting-the-block-mev-boost-compatibility-and-relays/19837)
- [XGA](https://docs.xga.com) - L2 Gas Auction platform.

## Articles

## Presentations

## Full Day Events

### ZuBerlin - 2024
- [Drew, Kubi, Lorenzo - Commit-Boost](https://streameth.org/zuberlin/watch?session=66681afef9b8e98b1ec95fdd) - Introducing the Commit-Boost effort, including a walkthrough of the code.
- [Daniel - LimeChain](https://streameth.org/zuberlin/watch?session=66684f7006eda795c8925909) - Dicusses how preconfirmations interact with the L1 PBS pipeline.
- [Conor - Switchboard](https://streameth.org/zuberlin/watch?session=66682e25f9b8e98b1ec98882) - Introduces Preconfirmations Sauna, a credibly neutral effort to standardise preconfirmations.
- [Harry - Luban](https://streameth.org/zuberlin/watch?session=6668652806eda795c89291b2) - Shares a lottery mechanism for pricing preconfirmations.
- [Jonas - Chainbound](https://streameth.org/zuberlin/watch?session=666828e8f9b8e98b1ec97e79) - Shares how Bolt enables L1 preconfirmations.
- [Christian - Primev](https://streameth.org/zuberlin/watch?session=66685ecd06eda795c8928664) - Shares how mev-commit enables L1 preconfirmations.
- [Tariz - Radius](https://streameth.org/zuberlin/watch?session=66686a3306eda795c892964e) - Shares how Radius integrates based sequencing.

## Implementations


## Related Concepts
- [Proposer-Builder Separation (PBS)](https://github.com/ethereum/builder-specs) - A related concept that separates the roles of proposers and builders in the Ethereum consensus layer.
- [MEV-Boost](https://boost.flashbots.net/) - A middleware that outsources block building to a network of builders, enabling proposer commitments.
- Embedded Rollups, [Part 1](https://ethresear.ch/t/embedded-rollups-part-1-introduction/21460) and [Part 2](https://ethresear.ch/t/embedded-rollups-part-2-shared-bridging/21461) - Posts exploring fast and efficient cross-chain interoperability by implementing an embedded shared-bridge rollup.

## Contributing
Contributions to this awesome list are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) before submitting a pull request.






