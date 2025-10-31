# zkShine JavaScript SDK

![Solana](https://img.shields.io/badge/Built_for-Solana-14F195?logo=solana&logoColor=white)
![Zero Knowledge](https://img.shields.io/badge/ZK-Privacy-blueviolet)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Version-0.1.0--alpha-yellow)

> Official JavaScript SDK for **zkShine**, enabling private transactions, confidential compute, and zk-based identity operations on **Solana**.

---

## 📦 Installation

```bash
npm install @zkshine/sdk
# or
yarn add @zkshine/sdk


Basic Usage
import { zkShine } from "@zkshine/sdk";

// Initialize SDK
const zk = await zkShine.init({
  network: "mainnet-beta", // or "devnet"
  rpc: "https://api.mainnet-beta.solana.com",
});

// Generate private keypair
const wallet = await zk.createWallet();

// Deposit assets into zk pool
await zk.deposit({
  from: wallet.publicKey,
  amount: 1.5,
  token: "SOL",
});

// Withdraw with privacy key
await zk.withdraw({
  to: "DestinationPublicKey",
  key: "user-private-zk-key",
});
