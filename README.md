<div align="center">
  <a href="https://github.com/akm2006">
    <img src="assets/avatar.png" width="96" height="96" alt="Aakash Mandal" style="border-radius: 16px; border: 2px solid #27272a;" />
  </a>
  <h1 align="center" style="margin-top: 14px; margin-bottom: 4px;">Aakash Mandal</h1>
  <p align="center">
    <strong>Systems &amp; Protocol Infrastructure Engineer</strong><br />
    <em>Non-Custodial Execution Layers &bull; Zero-Knowledge Settlement &bull; Autonomous Payment Rails &bull; Embedded DSP</em>
  </p>
  <p align="center">
    <a href="https://x.com/aakashbeyond"><img src="https://img.shields.io/badge/X-@aakashbeyond-09090b?style=flat-square&logo=x&logoColor=white&labelColor=18181b" alt="X @aakashbeyond" /></a>
    <a href="mailto:aakashmandal10@gmail.com"><img src="https://img.shields.io/badge/Email-aakashmandal10@gmail.com-09090b?style=flat-square&logo=gmail&logoColor=white&labelColor=18181b" alt="Email" /></a>
    <a href="https://www.linkedin.com/in/aakash-mandal"><img src="https://img.shields.io/badge/LinkedIn-aakash--mandal-09090b?style=flat-square&logo=linkedin&logoColor=0A66C2&labelColor=18181b" alt="LinkedIn" /></a>
    <img src="https://img.shields.io/badge/Location-Kolkata%2C%20India-09090b?style=flat-square&logo=google-maps&logoColor=EA4335&labelColor=18181b" alt="Location" />
    <img src="https://img.shields.io/badge/Focus-Core%20%26%20Protocol%20Engineering-ffd600?style=flat-square&logoColor=black&labelColor=18181b" alt="Focus" />
  </p>
</div>

---

### ⚡ Signal Architecture & Focus Areas

Building high-throughput SVM instruction parsers, confidential Soroban protocols, and scoped smart account execution layers where users never surrender capital custody.

| Metric / Dimension | Implementation & Architecture | Technical Moat |
| :--- | :--- | :--- |
| **Sub-200ms Feed** | **Solana SVM Yellowstone gRPC Ingestion** | Custom Rust Carbon instruction parser & Redis atomic deduplication |
| **On-Chain ZK Verifier** | **Stellar Soroban Shielded Vault** | Circom Groth16 circuit proofs over native Soroban BN254 host functions |
| **Autonomous Rails** | **Machine-to-Machine HTTP Micropayments** | Stateless x402 protocol + scoped MetaMask ERC-7710/7715 delegations |
| **IoT Telemetry** | **ESP32 True RMS AC Power DSP** | Discrete C++ signal processing with noise-gating & MQTT WebSockets loop |

---

### 🚀 Flagship Systems & Protocol Deployments

#### 1. [Stellalpha](https://stellalpha.xyz) — Autonomous Non-Custodial Intent & Execution Layer
> *Sub-second trade intent detection and allocation-weight execution on Solana SVM.*

- **Problem:** Copy-trading bots blindly mirror raw wallet transactions. Heterogeneous follower balances cause catastrophic portfolio drift, front-running slippage, and custodial key risk.
- **Architecture:** 
  - Dual ingestion pipeline pairing **Yellowstone gRPC** (~200ms signature capture) with **Helius Enhanced Webhooks** and Upstash Redis atomic locks.
  - Custom Rust **SevenLabs Carbon SVM parser** decoding instructions at the source for Jupiter, Raydium, and Meteora.
  - On-chain Anchor vault program (`stellalpha_vault`) implementing isolated `UserVault -> TraderState` PDAs with delegated Jupiter swap policies (zero withdrawal rights).
  - Asymmetric execution policy that drops stale BUYs older than 10s while guaranteeing exits.
- **Tech Stack:** `Solana SVM` &bull; `Rust` &bull; `Anchor` &bull; `Yellowstone gRPC` &bull; `SevenLabs Carbon` &bull; `Jupiter SDK` &bull; `Redis` &bull; `TypeScript`
- **Verified Links:** [Live App (stellalpha.xyz)](https://stellalpha.xyz) &bull; [App Repository](https://github.com/akm2006/stellalpha) &bull; [Vault Program Repository](https://github.com/akm2006/stellalpha_vault) &bull; [Whitepaper (PDF)](https://stellalpha.xyz/whitepaper.pdf) &bull; [DoraHacks BUIDL](https://dorahacks.io/buidl/32072)

---

#### 2. [Vayyl](https://vayyl.vercel.app) — Confidential Settlement Infrastructure for Stellar Soroban
> *Zero-knowledge private balance and shielded settlement pools on native Soroban BN254.*

- **Problem:** Public ledgers turn every treasury movement, trade strategy, supplier payment, and payroll transfer into permanently exposed public metadata.
- **Architecture:**
  - Shielded pool contracts on Soroban enabling users to deposit public XLM, hold encrypted note commitments, and withdraw to unlinked addresses via ZK proofs.
  - Circom Groth16 circuits using Poseidon2 hashing for note commitments and nullifier generation, verified on-chain via **native Soroban BN254 host functions**.
  - Client-side browser Web Worker proof generation inside Next.js (zero private key or witness data leaves the client device).
  - Decoupled transaction relayer service deployed on Railway for fee-bumped anonymous withdrawals.
- **Tech Stack:** `Stellar Soroban` &bull; `Rust` &bull; `Circom 2.x` &bull; `Groth16` &bull; `Poseidon2` &bull; `BN254 Host Functions` &bull; `snarkjs` &bull; `Railway`
- **Verified Links:** [Live DApp (vayyl.vercel.app)](https://vayyl.vercel.app) &bull; [Protocol Docs Repository](https://github.com/akm2006/Vayyl-docs) &bull; [Testnet Fixed-Note Pool Contract](https://stellar.expert/explorer/testnet/contract/CBUNTVFHCNN5CYNA3TLTSWPVYX5ED5V6W6X3Y5EAHUOZYJRUPYNAX33A)

---

#### 3. [TaskMarket402](https://github.com/akm2006/TaskMarket402) — Mission Budget WorkGraph for Autonomous Agent Teams
> *Connecting scoped MetaMask permissions to machine-to-machine x402 HTTP micropayments.*

- **Problem:** Multi-agent autonomous swarms either require manual user signatures for every subtask API call or demand dangerous full private key custody.
- **Architecture:**
  - Single bounded budget permission granted via **MetaMask Smart Accounts** (ERC-7715 / ERC-7710 / EIP-7702).
  - Manager Agent splits mission budgets into sub-budgets and delegates payments to specialist agents (Contract Scanner, Wallet Profiler, Market Context).
  - Integrated **x402 HTTP payment protocol** on Base Sepolia for stateless machine-to-machine paid API endpoints without human re-signing.
  - Interactive ReactFlow WorkGraph rendering real-time budget trails, payment receipts, and blocked safety gates.
- **Tech Stack:** `ERC-7710` &bull; `ERC-7715` &bull; `x402 Protocol` &bull; `MetaMask Smart Accounts` &bull; `Base Sepolia` &bull; `ReactFlow` &bull; `TypeScript`
- **Verified Links:** [Code Repository](https://github.com/akm2006/TaskMarket402) &bull; *Proven on Base Sepolia Testnet*

---

#### 4. ProofDrop — ZK Private Eligibility & Anti-Duplicate Claim Protocol
> *Poseidon Merkle membership proofs and on-chain nullifiers on Stellar Soroban.*

- **Problem:** Distributing grants, scholarships, or airdrops requires validating user eligibility without exposing identity, while strictly preventing duplicate claims (Sybil resistance).
- **Architecture:**
  - Circom eligibility circuits proving knowledge of a secret committed to a Poseidon Merkle tree without revealing the leaf index or recipient identity.
  - Soroban smart contracts atomically verifying Groth16 proofs, registering nullifier hashes, and rejecting duplicate claims with error `NullifierAlreadyUsed`.
- **Tech Stack:** `Circom 2.x` &bull; `SnarkJS` &bull; `Poseidon Merkle Tree` &bull; `Stellar Soroban` &bull; `Rust` &bull; `Freighter`
- **Verified Links:** [Verified Claim Transaction](https://stellar.expert/explorer/testnet/tx/ff7ba75035894be52b70f3856cd772cb5e6d6077ccaad9913d20ee5034848197) &bull; [Verifier Contract](https://stellar.expert/explorer/testnet/contract/CAL5F45XD77LBE52HOHM6AFC3S6LH4LV767ONRHHR6PFAFZT5IW6T3ZU) &bull; [Campaign Contract](https://stellar.expert/explorer/testnet/contract/CC2MFYRDIMCTFUZACW5MG3OO4MTDQOVXWJTZ5J24PW7WAC4D3TOKQ3SO)

---

#### 5. [WattWave](https://wattwave.vercel.app) — IoT Energy Telemetry & Control Plane
> *Full-stack IoT energy monitoring system with True RMS AC DSP and MQTT WebSockets command center.*

- **Problem:** Monitoring real-time power consumption and remote appliance switching typically relies on closed proprietary hardware with high latency.
- **Architecture:**
  - Custom ESP32 C++ firmware with continuous ADC sampling calculating **True RMS AC voltage, current, active power, and power factor**.
  - Software noise-gating filter eliminating ADC offset drift and sensor idle noise.
  - Bidirectional **MQTT over WebSockets** pipeline enabling millisecond-latency telemetry reporting and instantaneous relay control.
- **Tech Stack:** `ESP32 (C++)` &bull; `FreeRTOS` &bull; `MQTT WebSockets` &bull; `Next.js 14` &bull; `Recharts` &bull; `Supabase`
- **Verified Links:** [Live App (wattwave.vercel.app)](https://wattwave.vercel.app) &bull; [Code Repository](https://github.com/akm2006/wattwave)

---

#### 6. [Synapse Yield](https://github.com/akm2006/synapse-yield) — Automated DeFi Yield Optimizer (Monad Testnet)
> *Scoped MetaMask keeper delegations and ERC-4337 UserOperations for non-custodial rebalancing.*

- **Problem:** Yield optimization across liquidity pools forces users to execute continuous manual transactions or surrender fund custody.
- **Architecture:**
  - Non-custodial automated yield rebalancer orchestrating staking positions across Kintsu (`sMON`) and Magma (`gMON`) on Monad Testnet.
  - Implemented the **MetaMask Delegation Toolkit** (ERC-7710) for scoped EIP-712 keeper permissions (rebalancing rights without withdrawal rights).
  - ERC-4337 UserOperation batching and submission via Pimlico bundler and EntryPoint contract.
- **Tech Stack:** `Monad Testnet` &bull; `ERC-4337` &bull; `MetaMask Delegation Toolkit` &bull; `Pimlico Bundler` &bull; `Envio Indexer` &bull; `Solidity`
- **Verified Links:** [Code Repository](https://github.com/akm2006/synapse-yield) &bull; [HackQuest Project Page](https://www.hackquest.io/projects/MetaMask-Smart-Accounts-x-Monad-Dev-Cook-Off-Synapse-Yield) &bull; [Demo Video](https://www.youtube.com/watch?v=LlatPV-aHzg)

---

### 🛠️ Systems & Cryptography Engineering Stack

```
Systems & Protocol  : Rust • Solana SVM • Anchor • Yellowstone gRPC • Carbon Parser • Stellar Soroban • Solidity • Foundry
Zero-Knowledge      : Circom 2.x • SnarkJS • Groth16 • Poseidon2 • Merkle Trees • Nullifiers • BN254 Host Functions
Autonomous Rails    : x402 Micropayments • MetaMask Smart Accounts (ERC-7715/7710) • 1Shot Relayer • Multi-Agent WorkGraphs
Telemetry & Runtime : ESP32 C++ • FreeRTOS • True RMS DSP • MQTT WebSockets • Next.js 15 • React 19 • TypeScript • Tailwind v4
```

<p align="left">
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Solana-9945FF?style=flat-square&logo=solana&logoColor=white" alt="Solana" />
  <img src="https://img.shields.io/badge/Soroban-000000?style=flat-square&logo=stellar&logoColor=white" alt="Soroban" />
  <img src="https://img.shields.io/badge/Circom_2.x-27272a?style=flat-square&logo=chainlink&logoColor=ffd600" alt="Circom" />
  <img src="https://img.shields.io/badge/Groth16_BN254-18181b?style=flat-square&logo=shield&logoColor=10b981" alt="ZK" />
  <img src="https://img.shields.io/badge/x402_Payments-ffd600?style=flat-square&logoColor=black&color=ffd600" alt="x402" />
  <img src="https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white" alt="Solidity" />
  <img src="https://img.shields.io/badge/Foundry-18181b?style=flat-square&logo=ethereum&logoColor=white" alt="Foundry" />
  <img src="https://img.shields.io/badge/ESP32_C++-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32" />
  <img src="https://img.shields.io/badge/Next.js_15-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
</p>

---

### 📦 Developer Tools & Open-Source Utilities

| Package / Repository | Description | Domain & Stack |
| :--- | :--- | :--- |
| [`smart-mailto`](https://github.com/akm2006/smart-mailto)<br>[![npm](https://img.shields.io/npm/v/smart-mailto?style=flat-square&color=cb3837)](https://www.npmjs.com/package/smart-mailto) | Zero-dependency TypeScript library providing smart webmail routing (Gmail, Outlook, Proton, Yahoo) with automated clipboard fallbacks. | **NPM Package**<br>`TypeScript` &bull; `React` |
| [`solana-wallet-cleaner`](https://github.com/akm2006/solana-wallet-cleaner) | Automated CLI utility scanning SPL and Token-2022 accounts: swaps dust to SOL via Jupiter, burns spam tokens, and closes empty ATAs to reclaim ~0.002 SOL rent per account. | **Solana Automation**<br>`Node.js` &bull; `Jupiter SDK` |
| [`0xGasless Smart Wallet Debugger`](https://github.com/akm2006/smart-wallet-controller) | Open-source GUI debugger for testing and executing 0xGasless smart accounts directly on Avalanche Mainnet with direct AgentKit controls. | **Developer Tooling**<br>`Viem` &bull; `@0xgasless/agentkit` |
| [`TP-Link Firmware Stripper`](https://github.com/akm2006/tplink-firmware-stripper)<br>[Live Web Tool](https://tplink-firmware-stripper.vercel.app) | Browser-based client binary buffer tool stripping 131,584-byte OEM bootloader headers for OpenWRT recovery, with an authoritative [Community Restoration Guide](https://github.com/akm2006/tplink-oem-restore). | **Embedded Firmware**<br>`Client Binary Buffer` |
| [`gatepass`](https://github.com/akm2006/gatepass) | Multi-role residential campus gate pass management system featuring tokenized multi-step approvals and real-time security QR check-in/out verification. | **Full-Stack Web**<br>`Next.js 15` &bull; `React 19` &bull; `MongoDB` |

---

### 📊 GitHub Activity & Telemetry

<div align="center">
  <a href="https://github.com/akm2006">
    <img src="https://streak-stats.demolab.com/?user=akm2006&theme=dark&background=09090b&border=27272a&stroke=ffd600&ring=ffd600&fire=ffd600&currStreakNum=ffd600&sideNums=e4e4e7&sideLabels=a1a1aa&dates=71717a" alt="GitHub Streak" width="85%" />
  </a>
</div>

<br />

<div align="center">
  <a href="https://github.com/akm2006">
    <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=akm2006&theme=github_dark" alt="GitHub Profile Details" width="85%" />
  </a>
</div>

---

<div align="center">
  <sub>"Engineering systems where users maintain complete capital custody and state transitions are mathematically verified."</sub><br />
  <sub>&copy; 2026 Aakash Mandal &bull; <a href="https://x.com/aakashbeyond">@aakashbeyond</a></sub>
</div>
