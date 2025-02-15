# TASK DESCRIPTION
## WHAT I DO IN THIS TASK :-Create and Deploy an ERC20 Token
#### we need a Web3 Wallet =Metamask ,Test ETH,A modern browser e.g.Chrome.
## What is an ERC20 token?
#### ERC stands for Ethereum Request for Comment, and 20 is the proposal identifier number. ERC-20 was designed to improve the Ethereum network.ERC-20 is one of the most significant ERCs. It has emerged as the technical standard for writing smart contracts on the Ethereum blockchain network, used for token implementation. ERC-20 contains a set of rules that all Ethereum based tokens must follow.
## Key Points about ERC-20 Tokens:
#### Standardized Functions: ERC-20 tokens follow a specific set of standards, which means they have a common list of rules and functions. This includes how the tokens can be transferred, how transactions are approved, how users can access data about a token, and the total supply of tokens.
#### Transferability and Exchange: These tokens can be transferred from one account to another as payment, similar to cryptocurrencies like Bitcoin, and can be traded on various cryptocurrency exchanges.
#### ERC-20 is a standard or guideline for creating new tokens. The standard defines six mandatory functions that a smart contract should implement and three optional ones.
#### The mandatory functions are listed below with explanations.
#### totalSupply: A method that defines the total supply of your tokens; when this limit is reached, the smart contract will refuse to create new tokens.
#### balanceOf: A method that returns the number of tokens a wallet address has.
#### transfer: A method that takes a certain amount of tokens from the total supply and gives it to a user.
#### transferFrom: Another type of transfer method that is used to transfer tokens between users.
#### approve: This method verifies whether a smart contract is allowed to allocate a certain amount of tokens to a user, considering the total supply.
#### allowance: This method is exactly the same as the approved method except that it checks if one user has enough balance to send a certain amount of tokens to another
# Creating Our Own Token:
## Getting Test ETH :
#### To begin deploying our contract on the Ethereum Sepolia testnet, we need to install the MetaMask browser extension. Once our wallet is set up,we need to acquire some test ETH.
#### I get faucets for Sepolia network for testing deployment on test network from [Link Text](https://cloud.google.com/application/web3/faucet)
## Writing the Smart Contract:
#### I use the OpenZeppelin ERC-20 contract to create our token. With OpenZeppelin, we don’t need to write the whole ERC-20 interface. Instead, we can import the library contract and use its functions.
#### Now I go to ethereum remix ide and make a new solidity file,( MyToken.sol)
### Write the following code into new Solidity script:
#### ```// SPDX-License-Identifier: MIT
#### pragma solidity ^0.8.20;
#### import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
#### contract MyToken is ERC20 {
####    constructor() ERC20("MyToken", "MT") {
####        _mint(msg.sender, 1000000 * (10 ** uint256(decimals())));
####    }
#### }```
#### ![Screenshot](![Screenshot 2025-02-15 164925](https://github.com/user-attachments/assets/5a704391-45b2-404a-9bcb-7ef89e6e8f5c)
# Deployment:
#### After completed the smart contract,proceed to compile it.
#### ![Screenshot 2025-02-15 170013](https://github.com/user-attachments/assets/02f8e164-5790-4a9c-9edc-ed088c2bca42)
#### Go to the Deploy & Run Transactions tab. For deployment, use the Injected Provider option under the Environment. Before the deployment, ensure that your MetaMask is set to the Sepolia testnet, and MyToken contract is the selected contract to be deployed. Finally, click on the Deploy button to deploy your contract.
#### ![Screenshot 2025-02-15 170741](https://github.com/user-attachments/assets/a7b7eab2-bfaf-493d-99bb-6c0579d2e52b)
####  Go to the Deploy & Run Transactions tab. For deployment, use the Injected Provider option under the Environment. Before the deployment, ensure that your MetaMask is set to the Sepolia testnet, and MyToken contract is the selected contract to be deployed. Finally, click on the Deploy button to deploy your contract.
#### Now,Confirm the transaction in metamask.
#### Our token contract is now deployed on Ethereum’s Sepolia testnet!
#### To see your contract on a blockchain explorer, a beginner-friendly useful tool used to analyze various blockchain data, go to the Etherscan Sepolia Explorer and search your contract's address.
#### ![Screenshot 2025-02-15 171808](https://github.com/user-attachments/assets/f56f88b4-c9e5-4355-8d43-586e70b7455c)
#### If we want to see your token in our MetaMask, copy the deployed contract’s address using the copy button near the contract’s name. Then, open MetaMask, click on the Import tokens button and paste the contract’s address in the Token contract address field. MetaMask will fetch the Token Symbol and decimals automatically. Click the Next and Import, and our token will be added to the wallet; it will be available under the assets section in Metamask.
#### ![Screenshot 2025-02-15 171410](https://github.com/user-attachments/assets/a978fd8e-f13f-4ecf-b541-dd49a73eebb2)




































