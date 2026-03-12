# 🎵 SplitNaira

> **Royalty splitting for Nigeria's creative economy — powered by Stellar**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Built on Stellar](https://img.shields.io/badge/Built%20on-Stellar-7B61FF)](https://stellar.org)
[![Soroban](https://img.shields.io/badge/Smart%20Contracts-Soroban-blueviolet)](https://soroban.stellar.org)
[![Wave Program](https://img.shields.io/badge/Stellar-Wave%20Program-blue)](https://drips.network/wave/stellar)

---

## 🌍 The Problem

Nigeria's creative economy is projected at **₦7.23 trillion in 2026** — spanning music, Nollywood films, Afrobeats, visual art, and podcasting. Yet behind every hit song or blockbuster film are multiple collaborators: producers, co-writers, directors, cinematographers, and managers — most of whom never receive their fair share.

Today, royalty distribution is:
- ❌ Handled manually via bank transfers prone to delays and disputes
- ❌ Opaque — collaborators have no visibility into how much was earned
- ❌ Centralized — a single rights holder controls all funds
- ❌ Slow — payments can take weeks or months after a release earns revenue

---

## ✅ The Solution

**SplitNaira** is a Web3 royalty distribution platform built on **Stellar** and **Soroban smart contracts**. It allows creative collaborators to:

1. **Define splits upfront** — set percentage ownership before a project is released
2. **Receive automatic payments** — when revenue flows in, Soroban instantly distributes to all collaborators
3. **Verify earnings transparently** — every payment is recorded on the Stellar blockchain
4. **Settle in XLM or USDC** — with optional off-ramp to Nigerian bank accounts

---

## 🎯 Target Users

| User Type | Use Case |
|---|---|
| 🎤 Musicians & Producers | Split streaming royalties among bandmates and studios |
| 🎬 Nollywood Filmmakers | Distribute box office and streaming revenue to cast & crew |
| 🎨 Visual Artists | Share NFT sale proceeds with collaborators |
| 🎙️ Podcasters | Split sponsorship income with co-hosts |
| 📱 Music Labels | Automate royalty payouts to signed artists |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js 14, TailwindCSS, TypeScript |
| Wallet Integration | Freighter Wallet, Stellar Wallets Kit |
| Smart Contracts | Soroban (Rust) on Stellar |
| Blockchain | Stellar Network (Mainnet + Testnet) |
| Backend | Node.js / Express API |
| Database | PostgreSQL (off-chain metadata) |
| Payments | Stellar USDC anchor + XLM |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────┐
│                  SplitNaira Web App                  │
│              (Next.js + TailwindCSS)                 │
└──────────────────────┬──────────────────────────────┘
                       │
         ┌─────────────▼──────────────┐
         │     Soroban Smart Contract  │
         │  - Split registry           │
         │  - Auto-distribution logic  │
         │  - Revenue tracking         │
         └─────────────┬──────────────┘
                       │
         ┌─────────────▼──────────────┐
         │       Stellar Network       │
         │  - XLM / USDC transfers     │
         │  - On-chain audit trail     │
         └────────────────────────────┘
```

---

## ✨ Key Features

### 🔀 Split Creation
- Create a royalty agreement for any creative project
- Assign percentage splits to any Stellar wallet address
- Lock splits before publishing (tamper-proof)

### 💰 Automatic Distribution
- Deposit earnings into the project's Soroban contract
- All collaborators receive their share in a single transaction
- Real-time balance dashboard per project

### 📊 Earnings Dashboard
- Track lifetime earnings per project
- View transaction history on Stellar Explorer
- Download CSV reports for accounting

### 🔔 Payment Notifications
- Email/SMS alerts when royalties land
- Webhook support for integrating with streaming platforms

### 🏦 Nigerian Off-Ramp (Roadmap)
- Convert XLM/USDC to NGN via local anchors
- Direct transfer to Nigerian bank accounts

---

## 🚀 Getting Started

### Prerequisites

- Node.js >= 18
- Rust & Cargo (for Soroban contracts)
- Stellar CLI
- Freighter Wallet browser extension

### Installation

```bash
# Clone the repository
git clone https://github.com/your-org/splitnaira.git
cd splitnaira

# Install frontend dependencies
cd frontend
npm install

# Install contract dependencies
cd ../contracts
cargo build

# Set up environment variables
cp .env.example .env
# Edit .env with your Stellar keys and API configs

# Run the development server
npm run dev
```

### Environment Variables

```env
NEXT_PUBLIC_STELLAR_NETWORK=testnet
NEXT_PUBLIC_CONTRACT_ID=your_soroban_contract_id
NEXT_PUBLIC_HORIZON_URL=https://horizon-testnet.stellar.org
DATABASE_URL=postgresql://localhost:5432/splitnaira
```

---

## 📁 Project Structure

```
splitnaira/
├── frontend/               # Next.js web application
│   ├── app/                # App router pages
│   ├── components/         # Reusable UI components
│   ├── lib/                # Stellar SDK helpers
│   └── styles/             # TailwindCSS styles
├── contracts/              # Soroban smart contracts (Rust)
│   ├── src/
│   │   ├── lib.rs          # Main contract logic
│   │   ├── splits.rs       # Split registry
│   │   └── distribute.rs   # Distribution logic
│   └── tests/              # Contract unit tests
├── backend/                # Node.js API server
│   ├── routes/             # API endpoints
│   └── services/           # Business logic
└── docs/                   # Documentation
```

---

## 🗺️ Roadmap

- [x] Project concept & architecture design
- [ ] Soroban smart contract (split registry + distribution)
- [ ] Freighter wallet integration
- [ ] Split creation UI
- [ ] Earnings dashboard
- [ ] Testnet deployment
- [ ] Nigerian NGN off-ramp integration
- [ ] Mobile-responsive PWA
- [ ] Mainnet launch
- [ ] Streaming platform webhook integrations (Audiomack, Boomplay)

---

## 🤝 Contributing

We welcome contributions from developers, designers, and creatives who care about fair pay in Nigeria's creative economy.

Please read our [CONTRIBUTING.md](./CONTRIBUTING.md) to get started.

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

## 🌟 Acknowledgements

- [Stellar Development Foundation](https://stellar.org) for the Wave Program
- [Soroban](https://soroban.stellar.org) for smart contract infrastructure
- Nigeria's creative community — the artists, producers, and filmmakers this is built for

---

<p align="center">Built with ❤️ for Nigeria's creative economy</p>
