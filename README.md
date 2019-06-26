
# Ethereum Election DAPP

The Ethereum Election DAPP is a web based application that allows different Ethereum accounts to vote for a candidate from a predetermined list. Each account is allowed to cast a vote only once.

This project uses Ganache CLI to run a local Ethereum blockchain with 10 accounts, each having an initial balance of 100 ETH. The smart contract is written in Solidity and the front end application is built using HTML, CSS and JavaScript. Testing script for the smart contract is written in JavaScript using Mocha test framework and Chai assertion library.

Follow the steps below to download, install and run this project.

## Dependencies
- NPM: https://nodejs.org
- Truffle: https://github.com/trufflesuite/truffle
- Ganache CLI: https://github.com/trufflesuite/ganache-cli
- Metamask: https://metamask.io/
- Solidity Syntax Highlighter for Code Editor (optional)

## Step 1. Clone Project
```
git clone https://github.com/UrvashiKishnani/ethereum-election-dapp
```

## Step 2. Install Dependencies
```
$ cd ethereum-election-dapp
$ npm install
```

## Step 3. Start Ganache
```
$ ganache-cli -p 8545
```
This will start a local blockchain instance. Copy the mnemonic provided by the command. The mnemonic will be a twelve word phrase.

## Step 4. Configure Metamask
In the Metamask extension within your browser, select `import using account seed phrase`, paste the mnemonic from the previous step and set a password. Select `Localhost 8545` from the list of networks. To add more accounts, click on the account picture on the top right corner and select `Create Account` from the dropdown menu. Up to 10 accounts with balances can be created.

## Step 5. Compile & Deploy Election Smart Contract
In a new terminal, run the following command
```
$ truffle migrate --reset
```
You must migrate the election smart contract each time your restart ganache.

## Step 6. Test Smart Contract (Optional)
```
$ truffle test
```

## Step 7. Run the Front End Application
```
$ npm run dev
```
If the webpage does not open automatically, visit this URL in your browser: http://localhost:3000

To interact with the application, first select an account from Metamask and cast vote from this account by choosing a candidate from the dropdown menu and clicking on `Vote` button. Now you can select another account from Metamask, refresh the page and cast the vote from this new account.

---
_This project was inspired by https://github.com/dappuniversity/election_
