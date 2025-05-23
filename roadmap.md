# Haveno Android App – Roadmap

<div align="center">
  <img src="haveno_mobile.png" alt="Mobile Logo" width="220"/>
</div>



## Project Overview

This project aims to build a fully open-source, privacy-preserving Android app for the [Haveno DEX](https://github.com/haveno-dex/haveno), allowing users to privately trade Monero and other assets on mobile. The app must support both standalone operation and remote desktop sync, enforce Tor-only communication, and include an integrated self-custodial wallet.

## App Modes

1. **Remote Client Mode**  
   - Connects to a user’s existing Haveno desktop node  
   - Allows cross-device trading, data sync, and account continuity

2. **Standalone Node Mode**  
   - Runs a full Haveno backend instance on the Android device  
   - Requires Monero and Tor integration on-device  
   - Designed for users without access to a desktop node

## Development Phases

### Phase 1: Foundations (Weeks 1–2)
- Analyze Haveno’s backend architecture (gRPC, services)
- Set up base Android project (preferably Jetpack Compose)
- Design app structure to support dual operation modes
- Prepare development and testing environment
- Create UI wireframes for core flows (wallet, trade, chat)

### Phase 2: Privacy and Backend Integration (Weeks 3–5)
- Integrate Tor routing using Orbot or InviZible
- Implement gRPC bridge for Haveno daemon communication
- Manage daemon lifecycle for standalone mode
- Ensure fallback behavior if Tor is unavailable

### Phase 3: Wallet and Trading Core (Weeks 5–8)
- Integrate a Monero wallet library (lightwallet preferred)
- Display wallet sync status and balances
- Implement order book display and trade initiation
- Handle offer creation, trade lifecycle, and escrow

### Phase 4: Communication and Authentication (Weeks 9–11)
- Implement secure trade chat functionality
- Add support for account/session authentication across devices
- Securely store wallet and session data locally
- Add encrypted config and identity protection

### Phase 5: Packaging and Community Testing (Weeks 12–13)
- Build reproducible APK
- Open-source full project on GitHub
- Write detailed README and contribution guidelines
- Include build instructions and FDroid metadata
- Submit to FDroid; optionally prepare Play Store release

## Tech Stack

- **Language**: Kotlin
- **UI**: Jetpack Compose
- **Networking**: gRPC over Tor
- **Wallet**: Monero RPC or lightwallet library
- **Privacy Routing**: Orbot / InviZible
- **Daemon Management**: Embedded Haveno backend (for standalone)

## Development Guidelines

- All network traffic must be routed through Tor
- Ensure builds are reproducible and transparent
- No analytics, telemetry, or tracking libraries
- Maintain a modular code structure (UI, network, wallet, Tor, etc.)
- Code should be testable, auditable, and community-friendly

## For support; Direct XMR Donations: <br>
<p align="center">
   <i>84AWnCLPUqVfKLaRPvFbkYNvoCxiNJkj7WRZNezrRPxGEggQ2CvdvnXarH31gM1xQs3GzrpQxj6J7PJ35P3ESiX4AsAdXcD</i> <br>
  <img src="https://github.com/user-attachments/assets/7e9c5541-0556-46c9-bd3b-6977abd558f0" width="150" />
</p>

