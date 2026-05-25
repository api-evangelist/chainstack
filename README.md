# Chainstack (chainstack)

Chainstack is a managed multi-chain blockchain RPC and node infrastructure platform supporting 70+ networks including Ethereum, Solana, Bitcoin, BNB Smart Chain, Polygon, Arbitrum, Optimism, Base, Avalanche, TON, TRON, Starknet, zkSync Era, Hyperliquid, Monad, and many more. The platform exposes a REST Platform API for organization, project, network, and node lifecycle management; JSON-RPC endpoints for every supported chain; a multi-chain Faucet API; real-time Solana streaming via Yellowstone gRPC; low-latency Trader Nodes via bloXroute BDN; archive data with full `debug` and `trace` namespaces; MEV protection; Flashblocks preconfirmations on Base (200 ms) and Optimism (250 ms); a Chainstack MCP server for AI agents; and a Marketplace of one-click installable apps with unified billing. Chainstack offers Global, Dedicated, Unlimited, and Trader node archetypes, plus self-hosted control-plane deployments. SOC 2 Type II certified with a 99.99 percent uptime SLA.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/chainstack/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Blockchain, Multi-Chain, RPC, Node Infrastructure, Web3, Crypto, Ethereum, Solana, Bitcoin, DeFi, MEV, Trader Node, Archive Data, MCP, AI Agents

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Plans (Headline)

| Plan | Monthly (annual) | Included RU/mo | RPS | Overage / 1M RU |
|---|---|---|---|---|
| Developer (Free) | $0 | 3M | 25 | $20 |
| Growth | $49 ($40) | 20M | 250 | $15 |
| Pro | $199 ($166) | 80M | 400 | $12.50 |
| Business | $499 ($416) | 200M | 600 | $10 |
| Enterprise | from $990 ($825) | 400M+ | unlimited | $5 |
| Pay-As-You-Go | custom | n/a | custom | $5 |

1 Request Unit (RU) = 1 full-node RPC request; archive-node requests cost 2 RU. See [plans/chainstack-plans-pricing.yml](plans/chainstack-plans-pricing.yml).

## Add-ons

- **Unlimited Node** — flat-fee RPS commitment ($149/mo at 25 RPS through $3,199/mo at 1000 RPS)
- **Yellowstone gRPC (Solana)** — $49/mo single stream through $449/mo for up to 10 streams
- **Dedicated Node** — starting at $678/mo, plus $0.50/hour compute on Pro+
- **Warp Transactions** — $0.15 per transaction

## APIs

### Chainstack Platform API
REST API at `api.chainstack.com` for managing organizations, projects, networks, and nodes. API-key authenticated.

**Human URL:** [https://docs.chainstack.com/reference/platform-api-getting-started](https://docs.chainstack.com/reference/platform-api-getting-started)

- [OpenAPI](openapi/chainstack-platform-api-openapi.yml)
- [JSON Schema — Node](json-schema/chainstack-node-schema.json)
- [JSON-LD](json-ld/chainstack-context.jsonld)
- [Naftiko Capability — Organization](capabilities/platform-organization.yaml)
- [Naftiko Capability — Projects](capabilities/platform-projects.yaml)
- [Naftiko Capability — Networks](capabilities/platform-networks.yaml)
- [Naftiko Capability — Nodes](capabilities/platform-nodes.yaml)
- [Naftiko Capability — Legacy Faucet](capabilities/platform-faucet.yaml)

### Chainstack Faucet API
Multi-chain testnet faucet for Hoodi, Sepolia, BNB Testnet, zkSync Testnet, Scroll Sepolia, and Polygon Amoy. JWT bearer-authenticated.

**Human URL:** [https://faucet.chainstack.com/](https://faucet.chainstack.com/)

- [OpenAPI](openapi/chainstack-faucet-api-openapi.yml)
- [Naftiko Capability — Funding](capabilities/faucet-funding.yaml)

### Chain RPC APIs

Each chain exposes the canonical JSON-RPC interface for its protocol via Chainstack-managed nodes (Global, Dedicated, Unlimited, or Trader). The OpenAPI specs below were merged from the Chainstack Developer Portal per-method fragments.

| Chain | Operations | OpenAPI | Capability |
|---|---|---|---|
| Ethereum (execution) | 40 | [openapi](openapi/chainstack-ethereum-node-api-openapi.yml) | [capability](capabilities/chain-ethereum-rpc.yaml) |
| Ethereum Beacon Chain | 31 | [openapi](openapi/chainstack-ethereum-beacon-chain-api-openapi.yml) | [capability](capabilities/chain-ethereum-beacon-chain-rpc.yaml) |
| Solana | 52 | [openapi](openapi/chainstack-solana-node-api-openapi.yml) | [capability](capabilities/chain-solana-rpc.yaml) |
| Bitcoin | 40 | [openapi](openapi/chainstack-bitcoin-node-api-openapi.yml) | [capability](capabilities/chain-bitcoin-rpc.yaml) |
| BNB Smart Chain | 43 | [openapi](openapi/chainstack-bnb-node-api-openapi.yml) | [capability](capabilities/chain-bnb-rpc.yaml) |
| Polygon | 36 | [openapi](openapi/chainstack-polygon-node-api-openapi.yml) | [capability](capabilities/chain-polygon-rpc.yaml) |
| Arbitrum | 51 | [openapi](openapi/chainstack-arbitrum-node-api-openapi.yml) | [capability](capabilities/chain-arbitrum-rpc.yaml) |
| Optimism | 48 | [openapi](openapi/chainstack-optimism-node-api-openapi.yml) | [capability](capabilities/chain-optimism-rpc.yaml) |
| Base | 60 | [openapi](openapi/chainstack-base-node-api-openapi.yml) | [capability](capabilities/chain-base-rpc.yaml) |
| Avalanche | 31 | [openapi](openapi/chainstack-avalanche-node-api-openapi.yml) | [capability](capabilities/chain-avalanche-rpc.yaml) |
| Fantom / Sonic | 30 | [openapi](openapi/chainstack-fantom-node-api-openapi.yml) | [capability](capabilities/chain-fantom-rpc.yaml) |
| Gnosis | 28 | [openapi](openapi/chainstack-gnosis-node-api-openapi.yml) | [capability](capabilities/chain-gnosis-rpc.yaml) |
| Cronos | 30 | [openapi](openapi/chainstack-cronos-node-api-openapi.yml) | [capability](capabilities/chain-cronos-rpc.yaml) |
| Aurora | 28 | [openapi](openapi/chainstack-aurora-node-api-openapi.yml) | [capability](capabilities/chain-aurora-rpc.yaml) |
| Ronin | 32 | [openapi](openapi/chainstack-ronin-node-api-openapi.yml) | [capability](capabilities/chain-ronin-rpc.yaml) |
| TRON | 156 | [openapi](openapi/chainstack-tron-node-api-openapi.yml) | [capability](capabilities/chain-tron-rpc.yaml) |
| TON | 59 | [openapi](openapi/chainstack-ton-node-api-openapi.yml) | [capability](capabilities/chain-ton-rpc.yaml) |
| Starknet | 11 | [openapi](openapi/chainstack-starknet-node-api-openapi.yml) | [capability](capabilities/chain-starknet-rpc.yaml) |
| zkSync Era | 15 | [openapi](openapi/chainstack-zksync-node-api-openapi.yml) | [capability](capabilities/chain-zksync-rpc.yaml) |
| Polygon zkEVM | 34 | [openapi](openapi/chainstack-polygon-zkevm-node-api-openapi.yml) | [capability](capabilities/chain-polygon-zkevm-rpc.yaml) |
| Hyperliquid (HyperCore + HyperEVM) | 185 | [openapi](openapi/chainstack-hyperliquid-node-api-openapi.yml) | [capability](capabilities/chain-hyperliquid-rpc.yaml) |
| Monad | 32 | [openapi](openapi/chainstack-monad-node-api-openapi.yml) | [capability](capabilities/chain-monad-rpc.yaml) |
| Plasma | 59 | [openapi](openapi/chainstack-plasma-node-api-openapi.yml) | [capability](capabilities/chain-plasma-rpc.yaml) |
| Tempo | 63 | [openapi](openapi/chainstack-tempo-node-api-openapi.yml) | [capability](capabilities/chain-tempo-rpc.yaml) |

## Common Properties

- [Website — chainstack.com](https://chainstack.com)
- [Portal — Developer Portal](https://docs.chainstack.com)
- [Documentation — Platform API Reference](https://docs.chainstack.com/reference/platform-api-getting-started)
- [Documentation — RPC API Reference](https://docs.chainstack.com/reference/getting-started)
- [Documentation — Build Better (Supported Protocols)](https://chainstack.com/build-better/)
- [Pricing](https://chainstack.com/pricing/)
- [Faucet](https://faucet.chainstack.com/)
- [Support](https://support.chainstack.com)
- [Feedback / Ideas](https://ideas.chainstack.com/)
- [Blog](https://chainstack.com/blog/)
- [Changelog](https://chainstack.com/changelog/)
- [Status Page](https://chainstack.status.io)
- [Terms of Service](https://chainstack.com/terms-of-service/)
- [Privacy Policy](https://chainstack.com/privacy-policy/)
- [Security](https://chainstack.com/security/)
- [GitHub Organization](https://github.com/chainstack)
- [LinkedIn](https://www.linkedin.com/company/chainstack/)
- [Twitter / X](https://x.com/chainstackhq)
- [Discord](https://discord.com/invite/Cymtg2f7pX)
- [YouTube](https://www.youtube.com/@Chainstack)

## Products

- [Global Nodes](https://chainstack.com/products/global-nodes/)
- [Dedicated Nodes](https://chainstack.com/products/dedicated-nodes/)
- [Unlimited Nodes](https://chainstack.com/products/unlimited-nodes/)
- [Trader Nodes](https://chainstack.com/products/trader-nodes/)
- [Yellowstone gRPC for Solana](https://chainstack.com/products/yellowstone-grpc/)

## SDKs and Tooling (selected)

- [Chainstack Developer Portal (source)](https://github.com/chainstack/dev-portal) — MDX docs, OpenAPI fragments
- [Chainstack Erigon](https://github.com/chainstack/erigon) — Ethereum efficiency-frontier client
- [Chainstack BSC Erigon](https://github.com/chainstack/bsc-erigon) — BNB Smart Chain Erigon fork
- [Chainstack OP Erigon](https://github.com/chainstack/op-erigon) — Optimism Erigon fork
- [Solana Prometheus Exporter](https://github.com/chainstack/solana-exporter)
- [Solana RPC Ruby Client](https://github.com/chainstack/solana-rpc-ruby)
- [MultiChain Python CLI Wrapper](https://github.com/chainstack/multichaincli)
- [Bitcoin Python JSON-RPC Wrapper](https://github.com/chainstack/bitcoincli)
- [web3.py Quorum Extension](https://github.com/chainstack/web3quorum)
- [Terraform Module for RKE2 on OpenStack](https://github.com/chainstack/terraform-openstack-rke2)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Chainstack Platform API](openapi/chainstack-platform-api-openapi.yml)
- [Chainstack Faucet API](openapi/chainstack-faucet-api-openapi.yml)
- [Chainstack Ethereum Node API](openapi/chainstack-ethereum-node-api-openapi.yml)
- [Chainstack Ethereum Beacon Chain API](openapi/chainstack-ethereum-beacon-chain-api-openapi.yml)
- [Chainstack Solana Node API](openapi/chainstack-solana-node-api-openapi.yml)
- [Chainstack Bitcoin Node API](openapi/chainstack-bitcoin-node-api-openapi.yml)
- [Chainstack BNB Smart Chain Node API](openapi/chainstack-bnb-node-api-openapi.yml)
- [Chainstack Polygon Node API](openapi/chainstack-polygon-node-api-openapi.yml)
- [Chainstack Arbitrum Node API](openapi/chainstack-arbitrum-node-api-openapi.yml)
- [Chainstack Optimism Node API](openapi/chainstack-optimism-node-api-openapi.yml)
- [Chainstack Base Node API](openapi/chainstack-base-node-api-openapi.yml)
- [Chainstack Avalanche Node API](openapi/chainstack-avalanche-node-api-openapi.yml)
- [Chainstack Fantom Node API](openapi/chainstack-fantom-node-api-openapi.yml)
- [Chainstack Gnosis Node API](openapi/chainstack-gnosis-node-api-openapi.yml)
- [Chainstack Cronos Node API](openapi/chainstack-cronos-node-api-openapi.yml)
- [Chainstack Aurora Node API](openapi/chainstack-aurora-node-api-openapi.yml)
- [Chainstack Ronin Node API](openapi/chainstack-ronin-node-api-openapi.yml)
- [Chainstack TRON Node API](openapi/chainstack-tron-node-api-openapi.yml)
- [Chainstack TON Node API](openapi/chainstack-ton-node-api-openapi.yml)
- [Chainstack Starknet Node API](openapi/chainstack-starknet-node-api-openapi.yml)
- [Chainstack zkSync Era Node API](openapi/chainstack-zksync-node-api-openapi.yml)
- [Chainstack Polygon zkEVM Node API](openapi/chainstack-polygon-zkevm-node-api-openapi.yml)
- [Chainstack Hyperliquid Node API](openapi/chainstack-hyperliquid-node-api-openapi.yml)
- [Chainstack Monad Node API](openapi/chainstack-monad-node-api-openapi.yml)
- [Chainstack Plasma Node API](openapi/chainstack-plasma-node-api-openapi.yml)
- [Chainstack Tempo Node API](openapi/chainstack-tempo-node-api-openapi.yml)

### JSON Schema

- [Chainstack Node Schema](json-schema/chainstack-node-schema.json)
- [Chainstack JSON-RPC Envelope Schema](json-schema/chainstack-jsonrpc-envelope-schema.json)

### JSON-LD

- [Chainstack Context](json-ld/chainstack-context.jsonld)

### Capabilities (Naftiko)

- [Platform — Organization](capabilities/platform-organization.yaml)
- [Platform — Projects](capabilities/platform-projects.yaml)
- [Platform — Networks](capabilities/platform-networks.yaml)
- [Platform — Nodes](capabilities/platform-nodes.yaml)
- [Platform — Legacy Faucet](capabilities/platform-faucet.yaml)
- [Faucet — Funding](capabilities/faucet-funding.yaml)
- [Chain — Ethereum RPC](capabilities/chain-ethereum-rpc.yaml)
- [Chain — Ethereum Beacon Chain](capabilities/chain-ethereum-beacon-chain-rpc.yaml)
- [Chain — Solana RPC](capabilities/chain-solana-rpc.yaml)
- [Chain — Bitcoin RPC](capabilities/chain-bitcoin-rpc.yaml)
- [Chain — BNB Smart Chain RPC](capabilities/chain-bnb-rpc.yaml)
- [Chain — Polygon RPC](capabilities/chain-polygon-rpc.yaml)
- [Chain — Arbitrum RPC](capabilities/chain-arbitrum-rpc.yaml)
- [Chain — Optimism RPC](capabilities/chain-optimism-rpc.yaml)
- [Chain — Base RPC](capabilities/chain-base-rpc.yaml)
- [Chain — Avalanche RPC](capabilities/chain-avalanche-rpc.yaml)
- [Chain — Fantom RPC](capabilities/chain-fantom-rpc.yaml)
- [Chain — Gnosis RPC](capabilities/chain-gnosis-rpc.yaml)
- [Chain — Cronos RPC](capabilities/chain-cronos-rpc.yaml)
- [Chain — Aurora RPC](capabilities/chain-aurora-rpc.yaml)
- [Chain — Ronin RPC](capabilities/chain-ronin-rpc.yaml)
- [Chain — TRON RPC](capabilities/chain-tron-rpc.yaml)
- [Chain — TON RPC](capabilities/chain-ton-rpc.yaml)
- [Chain — Starknet RPC](capabilities/chain-starknet-rpc.yaml)
- [Chain — zkSync Era RPC](capabilities/chain-zksync-rpc.yaml)
- [Chain — Polygon zkEVM RPC](capabilities/chain-polygon-zkevm-rpc.yaml)
- [Chain — Hyperliquid RPC](capabilities/chain-hyperliquid-rpc.yaml)
- [Chain — Monad RPC](capabilities/chain-monad-rpc.yaml)
- [Chain — Plasma RPC](capabilities/chain-plasma-rpc.yaml)
- [Chain — Tempo RPC](capabilities/chain-tempo-rpc.yaml)

### Plans, Rate Limits, and FinOps

- [Plans and Pricing](plans/chainstack-plans-pricing.yml)
- [Rate Limits](rate-limits/chainstack-rate-limits.yml)
- [FinOps (FOCUS-aligned)](finops/chainstack-finops.yml)

### Vocabulary and Rules

- [Vocabulary](vocabulary/chainstack-vocabulary.yml)
- [Spectral Rules](rules/chainstack-rules.yml)
