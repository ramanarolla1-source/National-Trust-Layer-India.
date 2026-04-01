# Glide: Invisible Infrastructure for the Avalanche Ecosystem
Overview
Glide serves as the abstraction layer for the Avalanche "Subnet-per-App" vision. While Subnets offer localized scalability, they often suffer from Liquidity Silos and UX Friction (the need for specific gas tokens and manual bridging). Glide eliminates these barriers using Atomic Guarding logic.

Key Technical Integrations
1. Subnet Gas Abstraction
Glide allows users on the C-Chain (or external chains) to interact with localized Subnets without holding the Subnet's native gas token.

Mechanism: Glide’s "Guarding" contracts on the C-Chain accept liquid assets (AVAX, USDC) and trigger the corresponding transaction on the destination Subnet.

2. Atomic Guarding via Avalanche Warp Messaging (AWM)
To ensure security and atomicity, Glide is exploring the use of Avalanche Warp Messaging (AWM).

The Logic: A transaction is only finalized on the destination Subnet once the "Atomic Guard" verifies the source-chain commitment. This prevents orphaned transactions and ensures a "Set and Forget" experience for the user.

3. EVM-Compatibility
Since Glide is built with Solidity, our core orchestration logic is 100% compatible with the Avalanche C-Chain and any EVM-based Subnet.

Current Development Status (Fuji Testnet)
[ ] Contract Porting: Transitioning core logic from Rust/Soroban to Solidity.

[ ] Deployment: Initial "Guard" contracts being prepared for deployment on Avalanche Fuji.

[ ] Subnet Pilot: [ ] Subnet Pilot: Designing a mock "Municipal Payments Subnet" for the India market to demonstrate invisible onboarding for non-crypto citizens paying utility bills with local digital assets.

Roadmap (Avalanche Track)
Phase 1: Deployment of Atomic Guarding contracts on Fuji C-Chain.

Phase 2: Integration with a localized Subnet using AWM for message verification.

Phase 3: Release of the Glide-AVAX SDK for Subnet developers.

---
Project Links
DoraHacks ID: 42143

Video Demo: Glide: Atomic Guarding for Stellar & Initia

GitHub Repository: ramanarolla1-source

Founder: Venkat

