# 📱 SolScan Mobile – React Native

A mobile Solana blockchain explorer built with React Native.

This app allows users to paste a Solana wallet public key and instantly view:

- SOL balance
- SPL token balances
- Recent transactions
- Transaction status
- Direct link to Solscan explorer

All data is fetched directly from the Solana Mainnet RPC.

---

## 🚀 Features

- 🔍 Search wallet by public key
- 💰 Fetch real-time SOL balance
- 🪙 View SPL token accounts
- 📜 View latest 10 transactions
- ⏱ Human-readable "time ago" formatting
- 🔗 Open transactions in Solscan
- 📱 Clean dark-themed mobile UI
- ## 🧪 Demo Mode

For quick testing, the app includes a **Demo** button.

When clicked, it automatically pre-fills a sample public wallet address (Toly's public key) so users can instantly explore real on-chain data without manually entering an address.

---

## 🛠 Tech Stack

- React Native
- TypeScript
- Solana JSON RPC API
- Fetch API
- React Native FlatList
- Solana Mainnet Beta

---

## ⚙️ How It Works

The app sends JSON-RPC POST requests to:

https://api.mainnet-beta.solana.com

It directly interacts with the Solana blockchain using the following RPC methods:

- `getBalance` → Fetches SOL balance (converted from lamports to SOL)
- `getTokenAccountsByOwner` → Retrieves SPL token accounts owned by the wallet
- `getSignaturesForAddress` → Fetches recent transaction signatures

To optimize performance, the app uses `Promise.all()` to fetch balance, tokens, and transactions concurrently.

Transaction timestamps are converted into human-readable "time ago" format on the client side.

All requests are stateless and read-only, meaning the app never handles private keys or sensitive wallet data.

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/solana-explorer-rn.git
cd solana-explorer-rn
npm install
npm expo start(to open in expo app)
