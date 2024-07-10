# Polygon1
## NFT Collection Project

This project involves generating an NFT collection, storing the assets on IPFS, deploying a smart contract on the Goerli Ethereum Testnet, and bridging the NFTs to the Polygon Mumbai network. The following steps provide a detailed guide to achieve this.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Prerequisites](#prerequisites)
3. [Step-by-Step Guide](#step-by-step-guide)
   - [Generate NFT Collection](#generate-nft-collection)
   - [Store Assets on IPFS](#store-assets-on-ipfs)
   - [Deploy Smart Contract](#deploy-smart-contract)
   - [Map NFT Collection](#map-nft-collection)
   - [Batch Mint NFTs](#batch-mint-nfts)
   - [Batch Transfer NFTs to Polygon Mumbai](#batch-transfer-nfts-to-polygon-mumbai)
   - [Approve and Deposit NFTs to Bridge](#approve-and-deposit-nfts-to-bridge)
   - [Test Balance on Mumbai](#test-balance-on-mumbai)
4. [Conclusion](#conclusion)

## Project Overview

This project demonstrates the process of creating and managing an NFT collection from generation to cross-chain transfers. We will:

1. Generate a 5-item NFT collection using DALLE 2 or Midjourney.
2. Store the generated items on IPFS using Pinata.cloud.
3. Deploy an ERC721 or ERC1155 smart contract on the Goerli Ethereum Testnet.
4. Implement a function on the contract to return the prompt used for image generation.
5. Optionally, map the NFT collection using the Polygon network token mapper.
6. Write scripts to batch mint and transfer NFTs.
7. Bridge the NFTs from Ethereum to Polygon Mumbai.

## Prerequisites

- Node.js and npm installed
- Hardhat installed
- Metamask wallet configured with Goerli and Mumbai Testnets
- Pinata.cloud account
- DALLE 2 or Midjourney account

## Step-by-Step Guide

### Generate NFT Collection

1. **Generate Images**: Use DALLE 2 or Midjourney to generate 5 unique images. Save these images locally.
   
2. **Save Prompts**: Record the prompts used for generating each image.

### Store Assets on IPFS

1. **Upload to Pinata**: 
   - Create a Pinata account and log in.
   - Upload each image to Pinata and note down the IPFS hashes.

### Deploy Smart Contract

1. **Create Smart Contract**: Develop an ERC721 or ERC1155 smart contract.
   
2. **Implement promptDescription Function**: Add a function `promptDescription(uint256 tokenId) public view returns (string memory)` to return the prompt for each NFT.

3. **Deploy to Goerli Testnet**:
   - Configure Hardhat for Goerli.
   - Deploy the contract using Hardhat.

### Map NFT Collection

*Note: This step is optional but helps in visualizing the NFTs on Polygon.*

1. **Polygon Token Mapper**: Use the Polygon network token mapper to map your NFT collection for better visualization.

### Batch Mint NFTs

1. **Hardhat Script**: Write a script using Hardhat to batch mint all 5 NFTs. ERC721A is recommended for efficient minting.

### Batch Transfer NFTs to Polygon Mumbai

1. **FxPortal Bridge**: Write a Hardhat script to batch transfer the minted NFTs from Ethereum to Polygon Mumbai using the FxPortal Bridge.

### Approve and Deposit NFTs to Bridge

1. **Approve NFTs**: Approve the NFTs for transfer.
   
2. **Deposit to Bridge**: Use the bridge deposit function to move the NFTs to Polygon Mumbai.

### Test Balance on Mumbai

1. **Check Balance**: Verify the balance of the NFTs on the Polygon Mumbai network using the `balanceOf` function.

## Conclusion

This project guide covers the end-to-end process of creating, deploying, and managing an NFT collection, including cross-chain transfers. By following these steps, you will have a functional NFT collection deployed on Goerli and bridged to Polygon Mumbai.

For any issues or contributions, feel free to open an issue or pull request on this repository.

---
