# ponsmcp-contracts

> EVM smart contracts for PonsMCP payment escrow and settlement on Robinhood Chain.

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Robinhood Chain](https://img.shields.io/badge/chain-Robinhood_Chain_4663-6c47ff)](https://robinhoodchain.blockscout.com)
[![Solidity](https://img.shields.io/badge/solidity-0.8.24-363636?logo=solidity)](https://soliditylang.org)

---

## Overview

This repo will contain the Solidity smart contracts powering PonsMCP's on-chain payment escrow and settlement layer on **Robinhood Chain** (chainId 4663). All AI agent transactions are settled transparently via these contracts, with USDG (6 decimals) as the settlement asset.

> Status: pre-launch — contract development in progress.

---

## Architecture (planned)

```
PonsMCPRegistry
  └── PaymentIntentFactory
        └── PaymentIntent (per transaction)
              ├── initializePaymentIntent()
              ├── finalizePaymentIntent()
              ├── cancelPaymentIntent()
              └── disputePaymentIntent()
```

---

## Contract Functions (planned)

| Function | Description |
|----------|-------------|
| `initializePaymentIntent` | Creates escrow and locks USDG funds |
| `finalizePaymentIntent` | Verifies delivery proof and releases funds to merchant |
| `cancelPaymentIntent` | Refunds funds after timeout expires |
| `disputePaymentIntent` | Initiates on-chain dispute resolution |
| `registerMerchant` | Adds merchant to verified registry |

---

## Getting Started

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)
- Node.js 18+

---

## Network

| Setting | Value |
|---------|-------|
| Chain | Robinhood Chain (Arbitrum Orbit L2) |
| Chain ID | `4663` |
| RPC | `https://rpc.mainnet.chain.robinhood.com` |
| Explorer | `https://robinhoodchain.blockscout.com` |
| $PONS token | `0x39dBED3a2bd333467115dE45665cC57F813C4571` |
| USDG | `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168` (6 decimals) |

---

## License

MIT — see [LICENSE](LICENSE).
