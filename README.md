# ShadowSwap Subgraph

TheGraph exposes a GraphQL endpoint to query the events and entities within the Core Chain and ShadowSwap ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.

## Subgraphs

1. **[Blocks](https://thegraph.com/legacy-explorer/subgraph/ShadowSwap/blocks)**: Tracks all blocks on Core Chain.

2. **[Exchange](https://nodereal.io/meganode/api-marketplace/ShadowSwap-graphql)**: Tracks all ShadowSwap Exchange data with price, volume, liquidity, ...

6. **[Pairs](https://thegraph.com/legacy-explorer/subgraph/ShadowSwap/pairs)**: Tracks all ShadowSwap Pairs and Tokens.

7. **[Shadow Puppet](https://thegraph.com/legacy-explorer/subgraph/ShadowSwap/pancake-squad)**: Tracks all Shadow Puppet  metrics with Owners, Tokens (including metadata), and Transactions.

11. **[SmartChef](https://thegraph.com/legacy-explorer/subgraph/ShadowSwap/smartchef)**: Tracks all ShadowSwap SmartChef (a.k.a. Syrup Pools) with tokens and rewards.

12. **[Timelock](https://thegraph.com/legacy-explorer/subgraph/ShadowSwap/timelock)**: Tracks all ShadowSwap Timelock queued, executed, and cancelled transactions.


14. **[ShadowChef (v2)](https://thegraph.com/hosted-service/subgraph/ShadowSwap/masterchef-v2)**: Tracks data for ShadowChefV2.


## Dependencies

- [Graph CLI](https://github.com/graphprotocol/graph-cli)
    - Required to generate and build local GraphQL dependencies.

```shell
yarn global add @graphprotocol/graph-cli
```

## Deployment

For any of the subgraph: `blocks` as `[subgraph]`

1. Run the `cd subgraphs/[subgraph]` command to move to the subgraph directory.

2. Run the `yarn codegen` command to prepare the TypeScript sources for the GraphQL (generated/*).

3. Run the `yarn build` command to build the subgraph, and check compilation errors before deploying.

4. Run `graph auth --product hosted-service '<ACCESS_TOKEN>'`

5. Deploy via `yarn deploy`.

