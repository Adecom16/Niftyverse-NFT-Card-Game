

# Niftyverse - Online Multiplayer Web3 NFT Card Game

![Gameplay](https://i.ibb.co/4P2C08x/image.png)


## Getting Started

Follow these instructions to set up the Web3 part of the project.

### Prerequisites

- Node.js and npm installed
- Hardhat installed globally
- Core wallet installed (Metamask alternative for Avalanche dApps)

### Web3 Setup Instructions

0. **Navigate to the web3 directory**  
   ```bash
   cd web3
   ```

1. **Initialize a new Hardhat project**  
   ```bash
   npx hardhat
   ```  
   - Choose `y` for creating a new project
   - Choose `TypeScript` for language
   - Press `Enter` for default settings

2. **Install necessary packages**  
   ```bash
   npm install @openzeppelin/contracts dotenv @nomiclabs/hardhat-ethers
   npm install --save-dev "hardhat@^2.12.0" "@nomicfoundation/hardhat-toolbox@^2.0.0"
   ```

3. **Install Core Wallet**  
   Install the [Core Wallet](https://chrome.google.com/webstore/detail/core/agoakfejjabomempkjlepdflaleeobhb) extension for your browser.  
   - **Turn on Testnet Mode**:  
     - Open the Core extension
     - Click the hamburger menu (top left)
     - Go to **Advanced**
     - Turn on **Testnet Mode**

4. **Fund your wallet**  
   Use the [Avax Faucet](https://faucet.avax.network/) to get test AVAX tokens for the Fuji test network.

5. **Create a `.env` file**  
   Specify a `PRIVATE_KEY` variable in the `.env` file.  
   To get the private key:
   - Open Core extension
   - Click the hamburger menu (top left) → Security and Privacy → Show Recovery Phrase  
   - Enter your password, copy the phrase  
   - Go to [wallet.avax.network](https://wallet.avax.network/) → Access Wallet → Choose Mnemonic Key Phrase  
   - Paste the phrase, then go to **Manage Keys** → View C-Chain Private Key → Copy and paste it into the `.env` file

6. **Hardhat Configuration**  
   - Copy the `hardhat.config.ts` file from the GitHub gist provided in the description.

7. **Deploy Script**  
   - Copy the `deploy.ts` script from the GitHub gist provided in the description.

8. **Niftyverse Smart Contract**  
   - Copy the `Niftyverse.sol` smart contract code from the GitHub gist provided in the description.

9. **Compile the contract**  
   ```bash
   npx hardhat compile
   ```

10. **Deploy the smart contract**  
    Deploy the smart contract to the Fuji test network:  
    ```bash
    npx hardhat run scripts/deploy.ts --network fuji
    ```
    - Move the `/artifacts/contracts/Niftyverse.json` file to the `/contract` folder in the frontend
    - Copy the address of the deployed contract from the terminal and paste it into the `/contract/index.js` file of the frontend application

## ⚙️ Tech Stack

- React.js
- Tailwind CSS
- Solidity
- Ethers.js
- Hardhat
- Web3Modal
- Avalanche Network
- Core Wallet

## 🔋 Features

- **Create and Join Live Battles**: Engage in live battles with friends by creating or joining battlegrounds.
- **Choose Your Battleground**: Select from four distinct battlegrounds to enhance your strategy.
- **Real-Time Battle**: Experience real-time synchronization to monitor every move made by your opponent.
- **Interactive Gameplay**: Enjoy a deeply immersive gaming experience designed to captivate and challenge.
- **Live Interaction with Smart Contracts**: Conduct real-time Web3 transactions with opponents to strategize and compete for Ethereum rewards in battles.

## Smart Contract Overview

The `Niftyverse` smart contract handles the game's token management and battle logic. It is an ERC-1155 contract with the following capabilities:

- **Token Management**: Supports minting and tracking of game tokens representing characters like DEVIL, GRIFFIN, FIREBIRD, etc.
- **Battle System**: Allows players to create and join battles, choose moves (attack/defend), and determine battle outcomes based on smart contract logic.
- **Player and Game Data**: Manages player registration, health, mana, and battle statistics.

## Deploying to the Avalanche Fuji Test Network

Ensure all instructions are followed precisely to deploy the contract and run the game successfully on the Avalanche Fuji test network.
