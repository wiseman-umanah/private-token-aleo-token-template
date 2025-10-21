# 🚀 Aleo Private Token Deployment

This project demonstrates the process of **deploying a private token smart contract on the Aleo blockchain**, using the [Private Token Workshop Template](https://github.com/AleoAlexander/private-token-workshop-token-template).  

It covers all key steps — from cloning the repo and modifying mint functions to deploying and verifying the contract on Aleo’s testnet.

---

## 📘 Overview

Aleo is a **privacy-focused blockchain** that allows developers to build zero-knowledge applications using **Leo**, its high-level programming language.  

This project shows how to:
- Clone and set up a Leo project
- Implement private and public mint functionality
- Test the contract locally using the Leo Playground CLI
- Deploy it to Aleo testnet using personal credentials
- Verify and interact with the deployed contract on-chain

---

## 🧱 Project Repository

Template used:  
👉 [AleoAlexander/private-token-workshop-token-template](https://github.com/AleoAlexander/private-token-workshop-token-template)

---

## ⚙️ Project Setup

### 1. Clone the Repository

```bash
git clone https://github.com/AleoAlexander/private-token-workshop-token-template
cd private-token-workshop-token-template
This repository contains a base token implementation written in Leo, designed to demonstrate private and public minting mechanisms.

✏️ Step 2: Complete the Mint Functionality
Inside the contract, you’ll find mint_private and mint_public functions.
You must complete the logic for both minting types — ensuring that:

Private minting securely issues tokens without revealing user balances.

Public minting allows visible mint transactions on the Aleo blockchain.

Example snippet (pseudo-logic):

rust
Copy code
function mint_private(recipient: address, amount: u64) {
    // logic to mint private tokens
    // store minted notes securely under recipient’s address
}

function mint_public(recipient: address, amount: u64) {
    // logic to mint tokens publicly visible on-chain
}
Once done, you can test the contract locally before deployment.

🧪 Step 3: Test the Contract (Playground CLI)
You can test functions directly via the Leo Playground or your local CLI.

Example test command:

bash
Copy code
leo run mint_public aleo1recipientaddress 100u64
Or for a private mint:

bash
Copy code
leo run mint_private aleo1recipientaddress 50u64
Each run simulates execution on Aleo’s virtual machine, allowing you to verify function logic, parameters, and resulting state changes.

🚀 Step 4: Deploying the Contract
Once testing is successful, deploy the contract using your private key, network, and endpoint.

Create an .env file (see .env.example below):

bash
Copy code
NETWORK=testnet
PRIVATE_KEY=APrivateKey1zkp87nXowvCUBJ8jZsciBDocGPQZngBq764iPbyoGtL14tx
ENDPOINT=https://api.explorer.provable.com/v1
Deploy command:
bash
Copy code
leo deploy <program_name> --network $NETWORK --private-key $PRIVATE_KEY --endpoint $ENDPOINT
Your contract will be published to the Aleo testnet.

✅ Deployed Program ID:
at19gfze50aue9e5qxw7qx6vh60k5h80ssxt2ptjmaq7ru4tcz2r5gqedsgsj

You can verify your deployment on the Aleo Explorer.

🔍 Step 5: Verify and Execute On-Chain
After deployment, interact with your live contract to ensure all functions are working.

Example execution command:

bash
Copy code
leo execute <program_name>.mint_public aleo1recipientaddress 100u64 \
--network $NETWORK --private-key $PRIVATE_KEY --endpoint $ENDPOINT
You can then check your transaction and program state using:

Explorer:
🔗 Aleo Blockchain Explorer

Enter your program ID to view transactions and state changes.

💧 Step 6: Request Testnet Tokens (Aleo Credits)
Before deploying or executing, you’ll need testnet tokens for gas fees.

Request them from either of these faucets:

Official Aleo Faucet

Puzzle Faucet

🧾 .env Example
bash
Copy code
# Environment Variables
NETWORK=testnet
PRIVATE_KEY=APrivateKey1zkp87nXowvCUBJ8jZsciBDocGPQZngBq764iPbyoGtL14tx
ENDPOINT=https://api.explorer.provable.com/v1
🔗 Useful Links
Resource	URL
Aleo Playground	https://play.leo-lang.org/
Faucet 1	https://faucet.aleo.org/
Faucet 2	https://dev.puzzle.online/faucet
Explorer	https://explorer.provable.com/
Template Repo	https://github.com/AleoAlexander/private-token-workshop-token-template

🧠 Summary
By following these steps, you successfully:

Cloned and customized the Aleo private token template.

Implemented both private and public mint functions.

Tested the contract logic using the Leo Playground CLI.

Deployed the contract using personal Aleo credentials.

Verified and interacted with the deployed program on-chain.

This process highlights the end-to-end lifecycle of building privacy-preserving smart contracts on Aleo — from development and local testing to live deployment.

👨‍💻 Author
Wiseman Umanah
Deployed Private Token on Aleo Testnet
Program ID: at19gfze50aue9e5qxw7qx6vh60k5h80ssxt2ptjmaq7ru4tcz2r5gqedsgsj
