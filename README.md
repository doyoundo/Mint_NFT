# MintNFT 
This example[^1] is to publish your own NFT (ERC-721 Token) on the Ethereum blockchain! In this example, we create and deploy ERC-721 smart contract on the Ropsten test network. Then, we use the smart contract to mint NFT.

## Basics
### Programs Used
1. [Alchemy](https://www.alchemy.com/)
2. [MetaMask](https://metamask.io/)
3. [Ropsten faucet](https://faucet.ropsten.be/)
4. [Pinata](https://www.pinata.cloud/)

## Steps
1. Install dotenv package and add .env file in the root directory.
   - Add your MetaMask private key and HTTP Alchemy API URL to it.
```
API_URL="https://eth-ropsten.alchemyapi.io/v2/your-api-key"
PRIVATE_KEY="your-metamask-private-key"
```
2. Time to deploy smart contract! Run the following command in the root directory.
```
npx hardhat run scripts/deploy.js --network ropsten
```
  - **hardhat environment must be set up!**

3. Go to the Ropsten etherscan and search for the newly, created contract address.
4. Edit nft-metadata.json file as you prefer. You may upload an image to pinata and change the image URL to the CID.
5. Update env.file.
```
API_URL = "https://eth-ropsten.alchemyapi.io/v2/your-api-key"
PRIVATE_KEY = "your-private-account-address"
PUBLIC_KEY = "your-public-account-address"
```
6. Update nftContract address accordingly in scripts/mint-nft.js.
7. Run transaction!
```
node scripts/mint-nft.js
```

[^1]: [Ethereum Tutorial](https://ethereum.org/en/developers/tutorials/how-to-write-and-deploy-an-nft/)
