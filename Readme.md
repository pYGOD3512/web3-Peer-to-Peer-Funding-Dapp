# Peer-to-Peer Fundraising DApp

This is a peer-to-peer fundraising decentralized application (DApp) built on the Thirdweb platform. It consists of two main folders: Fundraising-client and Fundraising-smart-contract.

## Deployment of Fundraising-smart-contract

To deploy the Fundraising smart contract, follow these steps:

1. Clone the repository and navigate to the Fundraising-smart-contract folder.
2. Run `npm install` to install all dependencies listed in the package.json file.
3. Create a .env file in the root folder and add the following line: `PRIVATE_KEY=<wallet account private key>`. Make sure to replace `<wallet account private key>` with your actual wallet account private key.
4. Obtain your private key from the MetaMask extension installed in your browser. If you don't have MetaMask installed, you can download it from [here](https://metamask.io/). After installing, create an account or use an existing one, then access the account details and select "Show Private Key" to copy your private key.
5. Paste your private key into the .env file.
6. Run `npm run build` in your terminal to compile the application.
7. Run `npm run deploy`. This will provide you with a deployment link which you will use to deploy the application on Thirdweb.
8. Switch your MetaMask network to the Sepolia Chain. If you're not already connected to the Sepolia Chain, you can do so by selecting "Network" in the MetaMask extension, enabling "Show Testnet", and choosing Sepolia from the list.
9. Visit the Sepolia Faucet [here](https://sepolia.net/faucet) to obtain free test ethers. Paste your account address and receive 0.5 test ethers.
10. Open the deployment link provided in your terminal and click "Deploy". If it's your first time, you'll need to connect your wallet and sign the contracts that pop up.

Congratulations! You have successfully deployed the smart contract on Thirdweb. You can now visit the dashboard to view your smart contract and interact with its functions using the user-friendly UI provided by Thirdweb.

## Deployment of Fundraising-client

To connect the client-side with the smart contract, follow these steps:

1. Navigate to the Fundraising-client folder and run `npm install` to install the dependencies.
2. Go to the src > context > index.tsx file and copy your deployment address from Thirdweb (where your contract is deployed).
3. Paste the deployment address into the useContract function on line 10.
4. Run `npm run dev` to start your application.


## Alternative Chain Configuration

In case you want to run the application on your desired chain, follow these steps:

1. Navigate to the `main.tsx` file in the `src` root of the Fundraising-client folder.
2. Change the import and `activeChain` variable to your desired chain.
3. Ensure to configure the `hardhat.config.ts` file in the smart contract to suit the desired chain.
4. Replace the `sepolia` configuration with the chain name and the URL with the RPC URL to that chain.


## Technologies Used

- Solidity: Programming language for writing smart contracts.
- Hardhat: Development environment for compiling, deploying, and testing smart contracts.
- React: JavaScript library for building user interfaces.
- Thirdweb: Platform for deploying decentralized applications.
- MetaMask: Browser extension for interacting with Ethereum blockchain and managing digital assets.
- Sepolia Chain: Testnet blockchain network used for testing smart contracts and applications.
- TypeScript: Programming languages for implementing client-side logic.
- Axios: Promise-based HTTP client for making API requests.



## License

This project is licensed under the [MIT License](LICENSE).