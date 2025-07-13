# DelhiFund
A crowdfunding smart contract for ETHGlobal New Delhi 2025.

## Overview
As a Solidity beginner, I built DelhiFund to explore Web3, using a crowdfunding template from Solidity by Example. I studied the code to understand Ether handling and time-based logic, customized the contract name and goal, and deployed it on Sepolia for ETHGlobal.

## Deployment
- **Network**: Sepolia Testnet
- **Contract Address**: [https://sepolia.etherscan.io/address/0xa37d8bf74096f0129a88728ba6c41935e552327b](https://sepolia.etherscan.io/address/0xa37d8bf74096f0129a88728ba6c41935e552327b)

## Features
- **Contribution**: Users can send ETH to fund a campaign.
- **Funding Goal**: Tracks a 1 ETH target with a deadline.
- **Withdraw/Refund**: Owner withdraws funds if the goal is met; contributors can claim refunds if it fails.
- **Security**: Uses OpenZeppelin’s `ReentrancyGuard` to prevent attacks.

## Code Breakdown
`DelhiFund.sol` implements a crowdfunding system:
- **Constructor**: Sets the owner and deadline based on a duration input (e.g., 7 days).
- **Contribute**: Accepts ETH, tracks contributions via a mapping, and emits a `Contributed` event.
- **Withdraw**: Allows the owner to withdraw funds post-deadline if the 1 ETH goal is met, using `nonReentrant` for security.
- **GetRefund**: Refunds contributors if the goal isn’t met, clearing their contribution.

I learned how `require` ensures safety, `block.timestamp` handles deadlines, and `ReentrancyGuard` prevents attacks. Deploying via Remix was straightforward.

## Files
- **`DelhiFund.sol`**: Defines the crowdfunding contract.
- **`LICENSE`**: MIT License, allowing open-source use.
- **`.gitignore`**: Node.js template with `artifacts/` for clean commits.
- **`README.md`**: This file, detailing my project and journey.

## Source
Built using [Solidity by Example’s crowdfunding template](https://solidity-by-example.org/app/crowd-funding/), licensed under MIT, with OpenZeppelin’s [ReentrancyGuard](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/security/ReentrancyGuard.sol).

## Learning Journey
Building DelhiFund was a thrilling step in my Web3 journey! Studying the contract taught me about Ethereum transactions, state management, and security. Deploying to Sepolia and verifying on Etherscan felt like a big win.

## Usage
- Compile and deploy `DelhiFund.sol` in Remix (Solidity 0.8.20) with a duration (e.g., 604800 for 7 days).
- Contribute ETH via MetaMask or Remix.
- After the deadline, the owner can withdraw if the goal is met, or contributors can claim refunds.
- Verify on Etherscan.

## License
Licensed under the MIT License—see [LICENSE](LICENSE).

## Contact
Email me at rishabhgupta78470@gmail.com or find me on X @rishabh_guptaz. Excited to connect at ETHGlobal New Delhi 2025!
