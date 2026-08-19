<div align="center">

# ⚡ TrapTrace

**Operational Diagnostics, Live RPC Inspector & Transaction Failure Resolver for Stellar Soroban Smart Contracts**

[![Releases](https://img.shields.io/badge/Release-v0.2.0-2FA98C?style=flat-square&logo=github)](https://github.com/TrapTrace/soroban-error-cli/releases)
[![Web Studio](https://img.shields.io/badge/Live%20Studio-Vercel-1B1F23?style=flat-square&logo=vercel&logoColor=white)](https://traptrace-explorer.vercel.app)
[![Catalog Entries](https://img.shields.io/badge/Verified%20Entries-10-E2984B?style=flat-square)](https://github.com/TrapTrace/soroban-error-index)
[![CI Status](https://img.shields.io/badge/CI%20Pipelines-Passing-2FA98C?style=flat-square)](https://github.com/TrapTrace)
[![License](https://img.shields.io/badge/License-MIT-1B1F23?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## 🎯 About TrapTrace

Soroban smart contract developers on Stellar frequently encounter cryptic WASM execution traps, VM budget overruns, state archival expirations, and simulation failures. 

**TrapTrace** is an end-to-end developer tooling platform designed to inspect, simulate, decode, and resolve Soroban transaction errors on-chain. Rather than just offering static documentation, TrapTrace provides an **active 3-tier operational diagnostic ecosystem**:

```
┌────────────────────────────────────────────────────────────────────────┐
│                         TRAPTRACE ECOSYSTEM                             │
├────────────────────────────┬───────────────────────────────────────────┤
│ 🛠️  traptrace-cli          │ Operational Python CLI tool (v0.2.0):     │
│    (Developer Terminal)    │ • Live JSON-RPC 2.0 network client        │
│                            │ • On-chain tx inspector & root-cause map  │
│                            │ • Pre-flight simulation debugger          │
│                            │ • Ranked fuzzy search & report exports    │
│                            │ • Contract storage & TTL auditor          │
├────────────────────────────┼───────────────────────────────────────────┤
│ 🌐  soroban-error-explorer │ Live Web Diagnostics Studio (Vercel):     │
│    (Browser Studio)        │ • Real-time Stellar Testnet connectivity  │
│                            │ • Live contract event & trap stream       │
│                            │ • Interactive tx hash & XDR debugger      │
│                            │ • Shareable permalinks & report exports   │
│                            │ • Automated error catalog lookup          │
├────────────────────────────┼───────────────────────────────────────────┤
│ 📖  soroban-error-index    │ Schema-validated Error Knowledge Base:    │
│    (Diagnostic Database)   │ • 10 testnet-verified seed entries        │
│                            │ • Automated testnet verification harness  │
│                            │ • Strict JSON Schema CI validation        │
│                            │ • Automated index-to-explorer sync pipeline│
└────────────────────────────┴───────────────────────────────────────────┘
```

---

## 📂 Core Repositories

| Repository | Description | Key Technologies |
|---|---|---|
| 🛠️ **[`soroban-error-cli`](https://github.com/TrapTrace/soroban-error-cli)** | Operational CLI tool providing `traptrace inspect`, `simulate`, `watch`, `storage`, and `explain`. | Python 3, JSON-RPC 2.0, XDR Decoder, Pytest |
| 🌐 **[`soroban-error-explorer`](https://github.com/TrapTrace/soroban-error-explorer)** | Web application & Live Diagnostics Studio deployed at [traptrace-explorer.vercel.app](https://traptrace-explorer.vercel.app). | React 18, Vite 5, Lucide, Stellar Testnet RPC |
| 📖 **[`soroban-error-index`](https://github.com/TrapTrace/soroban-error-index)** | Foundational catalog containing testnet-verified error reproduction steps and remedies. | Markdown, YAML Frontmatter, JSON Schema |

---

## ⚡ Quickstart

### 1. Install and Run the CLI Diagnostic Tool
```bash
# Clone and install locally (or via pip)
git clone https://github.com/TrapTrace/soroban-error-cli.git
cd soroban-error-cli
pip install -e .

# Inspect an on-chain transaction hash and map failure root causes
traptrace inspect <TX_HASH> --network testnet

# Run pre-flight simulation for transaction envelope XDR
traptrace simulate <BASE64_XDR> --network testnet

# Check contract storage keys and remaining TTL ledgers before archival
traptrace storage --contract <CONTRACT_ID> --network testnet

# Search error codes and verified fixes
traptrace explain budget-exceeded
```

### 2. Use the Web Diagnostics Studio
Visit **[traptrace-explorer.vercel.app](https://traptrace-explorer.vercel.app)** to debug transactions, simulate XDR envelopes, and explore verified error fixes directly in your browser.

---

## 🤝 Drips Wave 8 & Community Contributions

TrapTrace is actively preparing for **Drips Wave 8 (Stellar Program)** with a structured community backlog of 16 scoped issues (2,500 points) covering:
- New testnet-verified error catalog entries (Host errors, Auth failures, WASM limits)
- Ranked fuzzy search algorithms
- Automated verification testnet harnesses
- Contributor templates and tooling extensions

We welcome issues and PRs! Please check the `CONTRIBUTING.md` guide in any repository to get involved.

---

<div align="center">
  <sub>Built for the Stellar Developer Ecosystem. Licensed under MIT. Copyright &copy; 2026 TrapTrace.</sub>
</div>
