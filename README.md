# EthEra

An Ethereum dapp for sending ETH with a message attached, and seeing every transfer on-chain.

- **`smart_contract/`:** a Solidity `Transactions` contract that records each transfer (sender, receiver, amount, message, keyword, time), built and deployed with Hardhat.
- **`client/`:** React + Vite + Tailwind front end. Connects MetaMask, sends transactions through `TransactionContext`, and lists past transfers.

## Run

```bash
# contract
cd smart_contract && npm install && npx hardhat run scripts/deploy.js --network <network>

# app
cd client && npm install && npm run dev
```

Put the deployed contract address in `client/src/utils/constants.js`.
