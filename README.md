
# InHaus Multi-Chain Staking Platform

![Project Logo](https://raw.githubusercontent.com/ArielRin/InHaus-Multichain-Staking-System-Public-Files/refs/heads/main/public/Assets/img1.png)

The Multi-Chain Staking Platform is a comprehensive staking system built to support multiple blockchain networks. It provides users and pool operators with a full-featured UI—including deploy-your-own staking pools, detailed staking pages, and customizable social links—and secure smart contracts designed to ensure safety and decentralization.


**Open the Dapp:** [Multi-Chain Staking Platform](https://inhaustemplate2025.netlify.app/)

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
  - [Multichain Support](#multichain-support)
  - [Staking Dashboard & Detailed Pages](#staking-dashboard--detailed-pages)
  - [Deploy Your Own Staking Pool](#deploy-your-own-staking-pool)
  - [Staking Actions: Deposit, Withdraw, Compound & Harvest](#staking-actions-deposit-withdraw-compound--harvest)
  - [Customizable User Profiles](#customizable-user-profiles)
- [Tutorials](#tutorials)
  - [How to Deploy a Staking Pool](#how-to-deploy-a-staking-pool)
  - [How to Stake in a Pool](#how-to-stake-in-a-pool)
- [Technical Architecture](#technical-architecture)
  - [Frontend & UI](#frontend--ui)
  - [Smart Contracts & Security](#smart-contracts--security)
- [Security & Ownership](#security--ownership)
- [Contribution Guidelines](#contribution-guidelines)
- [License](#license)
- [Contact & Social](#contact--social)

---

## Overview

The Multi-Chain Staking Platform is designed to empower both developers and end-users with a decentralized, multi-network staking experience. Whether you want to deploy your own staking pool or participate in existing ones, our platform offers a seamless and secure interface. It includes:

- **Multi-chain support:** Operate across different blockchains with native UI adaptations.
- **Dynamic dashboard:** Toggle between card and table view for an optimal user experience.
- **Staking actions:** Intuitive controls for depositing, withdrawing, compounding, and harvesting rewards.
- **Deployer responsibility and fee structure:** Every pool operator is responsible for their own pool, with transaction fees of approximately $0.25–$0.50 per staking function directed to the deployer treasury.
- **Customizable pool pages:** Personalize your staking pool with custom images, social links, and branding.

![Dashboard Screenshot](https://example.com/images/staking-dashboard.png)

---

## Key Features

### Multichain Support

- **Cross-Network Functionality:** The platform supports multiple blockchain networks, enabling users to stake tokens on different chains effortlessly.
- **Network Toggle:** Users can easily filter staking pools based on their connected network via a toggle switch.
- **Automatic Network Detection:** The system identifies the connected chain and validates staking actions based on the pool’s network.

### Staking Dashboard & Detailed Pages

- **Responsive UI:** A modern dashboard that switches between **Card View** and **Table View** to display pool details.
- **Staking Details:** Each pool page includes detailed information such as APR, TVL, user staking position, pending rewards, and network-specific details.
- **Extended Information Panel:** Expandable sections in table view offer additional insights into pool performance and user-specific staking data.

### Deploy Your Own Staking Pool

- **Pool Deployment:** Allow pool operators to create their own staking pools with customizable parameters.
- **Deployer Treasury:** A built-in fee mechanism collects a small transaction fee (approx. 25–50 cents per function call) that is routed directly to the deployer’s treasury.
- **Ownership & Accountability:** The system ensures that the pool deployer retains control and responsibility over their pool operations.

### Staking Actions: Deposit, Withdraw, Compound & Harvest

- **Deposit & Withdraw:** Integrated controls (with modals for a clean UX) enable users to deposit or withdraw tokens seamlessly.
- **Compound & Harvest:** Two distinct functions:
  - **Compound:** Automatically reinvests earned rewards into the staking pool.
  - **Harvest:** Allows users to claim rewards directly.
- **Action Validation:** Prior to executing any staking function, the system verifies that the user is connected to the correct network.

### Customizable User Profiles

- **Customized Pool Pages:** Pool operators can add personalized images, social media links, and custom branding to their pool pages.
- **Interactive Elements:** Social links and images can be updated to showcase community and project presence, enhancing trust and engagement.

---

## Tutorials

### How to Deploy a Staking Pool

1. **Connect Your Wallet:** Begin by connecting your wallet to the platform. The system automatically detects your network.
2. **Configure Pool Parameters:** On the "Deploy Your Staking Pool" page, enter details such as the staked token address, reward token address, APR, and duration.
3. **Review Fee Structure:** Note that a small transaction fee (approximately $0.25–$0.50 per function call) is applied. This fee goes to your deployer treasury.
4. **Deploy the Pool:** Submit the transaction to deploy the pool. Once confirmed, your pool will be live and visible on the main dashboard.
5. **Customize Your Page:** Edit your pool’s page by adding custom images and social links to enhance user trust.

*For a video tutorial, watch [Deploy Your Own Staking Pool](https://example.com/deploy-tutorial).*

### How to Stake in a Pool

1. **Browse Available Pools:** Use the toggle switch to filter pools by your connected network or view all pools.
2. **Select a Pool:** Click on a pool card or table row to view detailed information.
3. **Deposit Tokens:** Use the deposit button (or modal pop-up) to enter the amount you wish to stake.
4. **Monitor Your Position:** Check your staking dashboard for updated staking position, pending rewards, and APR.
5. **Manage Rewards:** Choose to compound your rewards or harvest them directly based on your investment strategy.

*For detailed step-by-step instructions, visit our [User Staking Guide](https://example.com/user-staking-guide).*

---

## Technical Architecture

### Frontend & UI

- **React & Material UI:** The user interface is built with React and Material UI, providing a responsive and modern design.
- **Dynamic Views:** Support for card and table views that let users easily toggle and filter pools.
- **Multi-Component System:** Components include the main ActiveStakingContractsPage, PoolCard, ExpandableRow, and modals for transactions.
- **Customizable Controls:** Integrated search, toggle switches, and network selectors for a user-friendly experience.

### Smart Contracts & Security

- **Smart Contract Design:**  
  - **Staking Contract:** Handles staking, rewards accumulation, compound functions, and harvesting.
  - **Deployer Contract:** Manages the deployment of individual staking pools. The deployer is held responsible for their own pool, with ownership controls to ensure accountability.
  - **Fee Mechanism:** Every transaction (deposit, withdraw, compound, harvest) includes a fee that is routed to the deployer’s treasury.
- **Security Measures:**  
  - **Ownership Compartmentalization:** The deployer retains exclusive control of their respective pool, reducing centralized risks.
  - **Audited Code Base:** Smart contracts undergo rigorous testing and auditing to ensure they are secure from common vulnerabilities.
  - **Network Checks:** UI interactions first verify that the user is connected to the correct blockchain network before executing functions.

---

## Security & Ownership

The security of our smart staking contracts is paramount. Our system is built on secure design principles including:

- **Decentralized Control:** Each staking pool is deployed by an independent operator who is responsible for the pool’s operations. This decentralizes risk and ensures accountability.
- **Fee Distribution:** A small transaction fee per staking function (ranging from 25 to 50 cents) is automatically allocated to the deployer treasury, ensuring that deployers have a financial incentive to maintain security.
- **Contract Audits:** Our contracts follow industry best practices and have been subjected to independent security audits. This process reduces the risk of exploits and vulnerabilities.
- **Harvest vs. Compound – An Essay:**

  In our system, **harvest** and **compound** serve distinct purposes. Harvesting allows users to claim accumulated rewards as they are earned. This function is ideal when users want to realize gains or use the rewards for other purposes. On the other hand, **compounding** reinvests the rewards into the staking pool, increasing the user’s stake and potentially enhancing future rewards exponentially through continuous reinvestment. Both methods have their advantages, and the choice depends largely on the user’s individual investment strategy and market conditions.

  The smart contracts implementing these functions incorporate safeguards such as reentrancy locks and strict validations to ensure that every function call is secure. The overall security framework, combined with the decentralized responsibility model of the deployer, reinforces the robust nature of the platform.

---

## Contribution Guidelines

We welcome contributions to enhance the platform. Please follow these guidelines:

- **Fork the Repository:** Create your own branch for new features or bug fixes.
- **Code Standards:** Follow our coding standards and write comprehensive tests.
- **Documentation:** Update or create documentation where necessary.
- **Pull Requests:** Submit pull requests with detailed descriptions of changes.
- **Security Audits:** Any changes impacting security should be double-checked and validated.

---

## License

This project is licensed under the MIT License. See the [LICENSE](https://example.com/license) file for details.

---

This README provides a complete overview of our multi-chain staking system, from user interface details and key features to deployment tutorials and a discussion on security. We hope that this document helps both developers and end-users understand and enjoy the full capabilities of our platform.
