# 🏛️ GovTrace

> **An immutable, blockchain-powered notary that prevents the manipulation of public infrastructure records and empowers citizen oversight.**

![Stellar](https://img.shields.io/badge/Stellar-Network-black?style=for-the-badge&logo=stellar)
![Soroban](https://img.shields.io/badge/Soroban-Smart_Contracts-orange?style=for-the-badge)
![Laravel](https://img.shields.io/badge/Laravel-11.x-FF2D20?style=for-the-badge&logo=laravel)
![Vue.js](https://img.shields.io/badge/Vue.js-3.x-4FC08D?style=for-the-badge&logo=vuedotjs)

## 🚨 The Problem

Billions of dollars are lost globally to abandoned public infrastructure projects ("white elephants"). The root cause of this impunity is the State's monopoly over digital records. Corrupt contractors and officials exploit centralized government databases by retroactively altering documents (backdating progress reports or suspension acts) right before an audit. This "administrative makeup" hides delays, encumbers investigations, and completely invalidates the physical evidence collected by citizens and NGOs.

## 💡 The Solution

**GovTrace** is a GovTech SaaS platform that acts as an automated, trustless digital notary. 

It integrates official open procurement data (SECOP API) with geo-tagged photographic evidence uploaded by citizens. The platform generates a cryptographic hash of this consolidated data and anchors it to the **Stellar Blockchain**. 

By creating a mathematically secured timestamp, GovTrace removes the State's monopoly on the truth. If a bad actor attempts to retroactively alter a public document in their centralized servers, GovTrace’s public verifier will instantly expose the manipulation. 

### Key Features
- **Walletless & Gasless UX:** Citizens don't need crypto wallets or tokens. The backend acts as a Relayer, sponsoring transaction fees via Stellar Launchtube.
- **Immutable Timestamping:** Evidence is anchored to the Stellar network, guaranteeing cryptographic proof of existence.
- **Universal Verifier:** Anyone can drag and drop a public document or evidence photo to instantly verify its integrity against the blockchain.

## 🏗️ Architecture

GovTrace follows a strict Clean Architecture pattern (Domain-Driven Design), isolating the Web3 infrastructure from the core business logic.

1. **Frontend (Vue 3 / TypeScript):** Citizen reporting dashboard and public verification portal.
2. **Backend API (Laravel 11 / PHP):** Handles API ingestion, evidence storage, and background processing via Redis queues.
3. **Web3 Bridge (Node.js / Stellar SDK):** A microservice that acts as the Relayer, signing transactions with a securely custodied private key.
4. **Blockchain (Stellar / Soroban):** The immutable ledger where SHA-256 hashes are permanently anchored.

## 🚀 Getting Started (Local Development)

This project uses Docker to ensure a frictionless setup process.

### Prerequisites
- [Docker & Docker Compose](https://www.docker.com/)
- [Node.js v20+](https://nodejs.org/)

### Installation

1. **Clone the repository**
   ```bash
   git clone [https://github.com/yourusername/govtrace.git](https://github.com/yourusername/govtrace.git)
   cd govtrace