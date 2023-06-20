# blockchain-101

How to build a Web3 dApp and the Blockchainexpert course at Algoexpert  

# Building a Web3 dApp - a decentralized art marketplace 

We are creating a decentralized marketplace, for digital art. 

## Smart contract 

Central to the dApp will be a "smart contract", that will be deployed on Ethereum. 

Example of a Smart Contract, written in Solidity: https://github.com/skirtapaieo/blockchain-101/blob/main/code/smart-contract.sol

## Front-end 

## Decentralized storage

## Identity 

## DAO 






# BlockchainExpert (course at Algoexpert.ai)

- [Web 1.0, 2.0, 3.0](#web-10-20-30)
- [Centralized vs Decentralized](#centralized-vs-decentralized)
  - [Centralized (controlled by a single entity)](#centralized-controlled-by-a-single-entity)
  - [Decentralized](#decentralized)
- [Ledgers](#ledgers)
- [Wallets](#wallets)
- [Transactions](#transactions) 

## Summary 

# web 1.0, 2.0, 3.0 

- Web 1.0 - read-only internet, no advertising 
- Web 2.0 - current state of web, centralized ownership, heavy advertising, front-end focus  
- Web 3.0 - idea around the future, decentralized control, more back-end focus

# centralized vs decentralized 

## Centralized (controlled by a single entity) 
- google 
- coinbase
- banks 
- amazon 
- US government 
- whats app 

## Decentralized
- Bitcoin 
- Ethereum 
- DeFi
- DAO's 
- IPFS
- Tor Network
- Decentralized Social Media (BlueSky)
- Open Source SW projects (often decentralized)

## Ledgers 

https://github.com/skirtapaieo/blockchain-101/blob/main/code/blockchain-ledger.py


## Wallets 

https://github.com/skirtapaieo/blockchain-101/blob/main/code/bitcoin-keys-and-address.py
https://github.com/skirtapaieo/blockchain-101/blob/main/code/encrypt-decrypt.py
https://github.com/skirtapaieo/blockchain-101/blob/main/code/wallet-example.py

## Transactions 

https://github.com/skirtapaieo/blockchain-101/blob/main/code/create-transaction.py

## Blocks 

Maz supply of Bitcoin is 21 M BTC, currently 19.1 is used. Satoshi Nakamoto inventor (pseudonym). A block is approximately 1 MB, and it is enough to store approx 2000 transactions. 
https://github.com/skirtapaieo/blockchain-101/blob/main/models/block.model.png

# Blockchain security 

- Decentralization makes it harder to compromise the network
- Cryptography used to secure data, digital signing using private key, all data is hashed
- 51% attack is when an entity controls more than 50% of Bitcoin mining hash rate (the processing power)

# Mining 

Mining is a process of creating new blocks on the Bitcoin blockchain

1. **Transaction Verification**. Miners start by picking up several unconfirmed transactions from the Bitcoin network's mempool. They check these transactions to ensure their validity.

Block Creation: They then compile these transactions into a 'block'. Along with the transaction data, each block contains the hash of the previous block (to maintain the chain's integrity) and a nonce.

Proof-of-Work: The miners' computers then try to find a nonce (a random number) that, when hashed with the rest of the content of the block, produces a hash with a certain number of leading zeroes (according to the current difficulty target). This step involves repeatedly changing the nonce and hashing the block until a suitable hash is found. This is the 'work' in Proof-of-Work.

Adding Block to the Chain: Once a miner finds a nonce that results in a suitable hash, they broadcast this block to the rest of the network. Other miners verify the block and, if it is valid, add it to their copies of the blockchain. This block is then considered 'confirmed'.

Reward: The miner who found the suitable hash is rewarded with newly minted Bitcoin (the block reward) and transaction fees from the transactions included in the block.

