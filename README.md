# agentcourt-bradbury
Trustless AI escrow protocol on GenLayer. Features LLM based consensus, deterministic code auditing, and automated smart settlement.
# ⚖️ AgentCourt Protocol

> **The First Autonomous Dispute Resolution & AI-Escrow Layer Built on GenLayer**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Network: Bradbury Testnet](https://img.shields.io/badge/GenLayer-Bradbury_Testnet-8b5cf6.svg)](https://genlayer.com)

Welcome to **AgentCourt**! 🚀 
Traditional escrow services and freelance platforms rely on slow, biased, and expensive human arbitrators to resolve disputes. AgentCourt changes the game by utilizing **GenLayer's Intelligent Contracts** to create a 100% trustless, AI-adjudicated settlement layer for digital workflows.

If you write code, deploy APIs, or build Web3 infrastructure, AgentCourt ensures you get paid fairly based on the *actual quality of your work*, audited on-chain by a decentralized network of Large Language Models (LLMs).

---

## 🧠 The GenLayer Edge: Why V2 is a Game Changer

Building AI into smart contracts isn't just about calling an API; it's about surviving decentralized consensus. In **AgentCourt V2** (optimized for the Bradbury Testnet), we solved the biggest hurdle of decentralized AI: **LLM Non-determinism**.

Instead of relying on fragile, character-by-character string matching (`strict_eq`), AgentCourt uses advanced **Tolerant Consensus** via `run_nondet_unsafe`. 
- Nodes independently run the code audit.
- They agree on *deterministic boundaries* (e.g., a score tolerance of ±8 and a Jaccard overlap of ≥60% for passed requirements).
- We extract the final verdict mathematically on-chain, preventing consensus timeouts while allowing heterogeneous LLMs across the validator network to express reasoning freely.

---

## ✨ Core Features

* 🤝 **Atomic Escrow:** Create cases, define custom development requirements (or pick from standard templates), and lock funds in a single transaction.
* 🤖 **Smart Code Auditor:** Providers submit an "Evidence Snapshot" (GitHub URL, API endpoint, etc.). GenVM reads the live evidence and audits it against the exact requirements.
* ⚖️ **Score-Based Settlement:** No more brutal "All-or-Nothing" outcomes. If the AI gives your project an 85% success score, the provider receives 85% of the escrow, and 15% is refunded to the buyer.
* 🛡️ **Structured Appeals:** Disagree with the AI? Submit a structured appeal pointing to a specific requirement (`e.g., R6`) with a new evidence URL for a re-audit.
* ⚡ **Event-Driven UI & Smart Cache:** The DApp is heavily optimized. It caches state metadata (`updated_at`) locally, dropping RPC requests by ~70% and ensuring lightning-fast UX.
* ⏱️ **Deadlock Prevention:** A built-in `force_finalize` mechanism ensures funds never get permanently stuck if a party abandons the case after the grace period.

---

## 🛠️ Technical Stack

* **Smart Contract:** Python (GenVM / `py-genlayer` SDK)
* **Frontend:** HTML5, Vanilla JavaScript, TailwindCSS
* **Web3 Connection:** `genlayer-js`
* **Network:** GenLayer Bradbury Testnet (Chain ID: 61999)

---

## 🚀 Quick Start (How to Test)

1. **Get a Web3 Wallet:** Install MetaMask or Rabby.
2. **Connect to Bradbury:** The DApp will automatically prompt you to switch to the **GenLayer Bradbury Testnet**.
3. **Get Testnet Tokens:** Use the GenLayer Studio Faucet to get test `GEN` tokens.
4. **Run the Frontend:** 
   Simply serve the `frontend/index.html` file using any local web server. (e.g., using Python: `python -m http.server 8000`)
5. **Play the Roles:**
   - **Buyer:** Create a case, select requirements (e.g., "OAuth2", "No SQL Injection"), and fund the escrow.
   - **Provider:** Switch wallets, submit your GitHub commit or API link.
   - **Court:** Hit "Request Smart Code Audit" and watch the decentralized AI nodes reach a consensus on your code quality!

---

## 🗺️ Roadmap (V3 Vision)

We are constantly pushing the boundaries of what AgentCourt can do. Our upcoming features include:
- **Milestone Escrow:** Linking multiple single-phase cases into a "Master Project" for UI-level milestone payouts.
- **Git Commit Snapshots:** Optional strict commit-hash binding for public repositories to guarantee 100% immutability.
- **Local On-Chain Reputation:** Scanning historical cases to display a Sybil-resistant success ratio for providers directly in the UI.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). Feel free to fork, build upon, and integrate AgentCourt into your own decentralized protocols.

*Built with ❤️ for the GenLayer Ecosystem.*
