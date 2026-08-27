<div align="center">

# ⚡ TrapTrace

**Operational Diagnostics, Live RPC Inspector & Transaction Failure Resolver for Stellar Soroban Smart Contracts**

[![Releases](https://img.shields.io/badge/Release-v0.3.0-2FA98C?style=flat-square&logo=github)](https://github.com/TrapTrace/soroban-error-cli/releases)
[![Web Studio](https://img.shields.io/badge/Live%20Studio-Vercel-1B1F23?style=flat-square&logo=vercel&logoColor=white)](https://traptrace-explorer.vercel.app)
[![Catalog Entries](https://img.shields.io/badge/Verified%20Entries-35%20(100%25)-E2984B?style=flat-square)](https://github.com/TrapTrace/soroban-error-index)
[![SDK Version](https://img.shields.io/badge/npm-%40traptrace%2Fsdk-CB3837?style=flat-square&logo=npm)](https://github.com/TrapTrace/traptrace-sdk)
[![CI Status](https://img.shields.io/badge/CI%20Pipelines-Passing-2FA98C?style=flat-square)](https://github.com/TrapTrace)
[![License](https://img.shields.io/badge/License-MIT-1B1F23?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## 🎯 About TrapTrace

Soroban smart contract developers on Stellar frequently encounter cryptic WASM execution traps, VM budget overruns, state archival expirations, and simulation failures. 

**TrapTrace** is an end-to-end developer tooling platform designed to inspect, simulate, decode, and resolve Soroban transaction errors on-chain. Rather than just offering static documentation, TrapTrace provides an **active 4-tier operational diagnostic ecosystem**:

```
┌────────────────────────────────────────────────────────────────────────┐
│                         TRAPTRACE ECOSYSTEM                             │
├────────────────────────────┬───────────────────────────────────────────┤
│ 🛠️  traptrace-cli          │ Operational Python CLI suite (v0.3.0):    │
│    (Developer Terminal)    │ • Live JSON-RPC 2.0 multi-network client  │
│                            │ • Multi-tx batch inspector (JSON datasets)│
│                            │ • Pre-flight simulation & TUI gas gauges  │
│                            │ • Contract auth tree hierarchy validator  │
│                            │ • Static contract AST linter & gas meter  │
│                            │ • Automated Rust code fix generator       │
│                            │ • Storage & state TTL expiration auditor  │
├────────────────────────────┼───────────────────────────────────────────┤
│ 🌐  soroban-error-explorer │ Live Web Diagnostics Studio (Vercel):     │
│    (Browser Studio)        │ • Real-time Stellar Testnet connectivity  │
│                            │ • Multi-transaction batch diagnostics     │
│                            │ • Auth hierarchy & signature validator    │
│                            │ • Contract WASM ABI & spec inspector      │
│                            │ • Smart contract linter & gas profiler    │
│                            │ • Rust test suite reproduction generator  │
│                            │ • Automated 35-entry verified catalog     │
├────────────────────────────┼───────────────────────────────────────────┤
│ 📦  @traptrace/sdk         │ TypeScript & JavaScript Client SDK:       │
│    (Developer Library)     │ • Offline bundled error catalog (35 rules)│
│                            │ • Diagnostic string parser & auto-fix     │
│                            │ • Invocation auth validator & TTL health  │
│                            │ • Soroban code linter & test generator    │
├────────────────────────────┼───────────────────────────────────────────┤
│ 📖  soroban-error-index    │ Schema-validated Error Knowledge Base:    │
│    (Diagnostic Database)   │ • 35 testnet-verified catalog entries     │
│                            │ • Automated testnet verification harness  │
│                            │ • Strict JSON Schema CI validation        │
│                            │ • Offline HTML documentation manual       │
└────────────────────────────┴───────────────────────────────────────────┘
```

---

## 📂 Core Repositories

| Repository | Description | Key Technologies |
|---|---|---|
| 🛠️ **[`soroban-error-cli`](https://github.com/TrapTrace/soroban-error-cli)** | Operational CLI suite providing `traptrace inspect`, `batch-inspect`, `simulate`, `auth-check`, `lint`, `profile`, `generate-test`, and `storage`. | Python 3, JSON-RPC 2.0, XDR Decoder, Pytest |
| 🌐 **[`soroban-error-explorer`](https://github.com/TrapTrace/soroban-error-explorer)** | Web application & Live Diagnostics Studio deployed at [traptrace-explorer.vercel.app](https://traptrace-explorer.vercel.app). | React 18, Vite 5, Lucide, Stellar Testnet RPC |
| 📦 **[`traptrace-sdk`](https://github.com/TrapTrace/traptrace-sdk)** | Client library for dApps, wallets, and IDE tooling to decode errors and profile transactions. | JavaScript, TypeScript (.d.ts), Node:test |
| 📖 **[`soroban-error-index`](https://github.com/TrapTrace/soroban-error-index)** | Foundational catalog containing 35 testnet-verified error reproduction steps and remedies. | Markdown, YAML Frontmatter, JSON Schema, Testnet Logs |

---

## ⚡ Quickstart

### Install the CLI Suite
```bash
pip install traptrace-cli
```

### Inspect On-Chain Failure
```bash
traptrace inspect <TX_HASH> --network testnet
```

### Run Static Contract Linter
```bash
traptrace lint contract/src/lib.rs
```

### Generate Rust Remediation Block
```bash
traptrace fix arith-error
```

---

<div align="center">
<sub>TrapTrace is an open-source public good for the Stellar Soroban ecosystem.</sub>
</div>
