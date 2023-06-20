# blockchain-101

How to build a Web3 dApp and the Blockchainexpert course at Algoexpert  

- [1. Building a Web3 dApp - a decentralized art marketplace](#1-building-a-web3-dapp---a-decentralized-art-marketplace)
  - [Smart contract](#smart-contract)
  - [Front-end](#front-end)
  - [Decentralized storage](#decentralized-storage)
  - [Identity](#identity)
  - [DAO](#dao)
- [2. BlockchainExpert (course at Algoexpert.ai)](#2-blockchainexpert-course-at-algoexpertai)
  - [Web 1.0, 2.0, 3.0](#web-10-20-30)
  - [Centralized vs Decentralized](#centralized-vs-decentralized)
    - [Centralized (controlled by a single entity)](#centralized-controlled-by-a-single-entity)
    - [Decentralized](#decentralized)
  - [Ledgers](#ledgers)
  - [Wallets](#wallets)
  - [Transactions](#transactions)
  - [Blocks](#blocks)
  - [Blockchain security](#blockchain-security)
- [3. Mining](#3-mining)
- [4. Consensus Mechanisms](#4-consensus-mechanisms)
  - [Proof of Work (PoW)](#proof-of-work-pow)
  - [Proof of Stake (PoS)](#proof-of-stake-pos)


# 1- Building a Web3 dApp - a decentralized art marketplace 

We are creating a decentralized marketplace, for digital art. 

## Smart contract 

Central to the dApp will be a "smart contract", that will be deployed on Ethereum. 

Example of a Smart Contract, written in Solidity: https://github.com/skirtapaieo/blockchain-101/blob/main/code/smart-contract.sol

## Front-end 

## Decentralized storage

## Identity 

## DAO 






# 2  BlockchainExpert (course at Algoexpert.ai)

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

## Blockchain security 

- Decentralization makes it harder to compromise the network
- Cryptography used to secure data, digital signing using private key, all data is hashed
- 51% attack is when an entity controls more than 50% of Bitcoin mining hash rate (the processing power)

# 3 - Mining 

Mining is a process of creating new blocks on the Bitcoin blockchain

**Requisites for mining** 

```
# Obtain necessary hardware
asic_miner = acquire_ASIC_miner()

# Install and set up Bitcoin client software
bitcoin_client = install_bitcoin_client()

# Synchronize the blockchain
blockchain = bitcoin_client.synchronize_blockchain()

# Ensure constant internet connection
internet_connection = ensure_internet_connection()

```


**Transaction Verification**
Miners pickup several unconfirmed transactions from the Bitcoin network's mempool.

```
# Fetch transactions from mempool
mempool_transactions = rpc_connection.getrawmempool()

# For each transaction in mempool
for txid in mempool_transactions:
    # Get the transaction details
    raw_tx = rpc_connection.getrawtransaction(txid)
    tx_details = rpc_connection.decoderawtransaction(raw_tx)
    
    # Verify the transaction
    # Note: In reality, Bitcoin nodes do this automatically
    if verify_transaction(tx_details):
        valid_transactions.append(tx_details)
```

**Block Creation** 
They then compile these transactions into a 'block'. 
```
# Create a new block with the valid transactions
new_block = create_new_block(valid_transactions)

```

**Proof-of-Work**
The miners' computers then try to find a nonce (a random number) that, when hashed with the rest of the content of the block, produces a hash with a certain number of leading zeroes (according to the current difficulty target). This step involves repeatedly changing the nonce and hashing the block until a suitable hash is found. This is the 'work' in Proof-of-Work.

```
# Try to solve the proof of work for the block
while not is_valid_proof(new_block):
    # Change the nonce
    new_block['nonce'] += 1

```


**Adding Block to the Chain** Once a miner finds a nonce that results in a suitable hash, they broadcast this block to the rest of the network. Other miners verify the block and, if it is valid, add it to their copies of the blockchain. This block is then considered 'confirmed'.

**Reward** The miner who found the suitable hash is rewarded with newly minted Bitcoin (the block reward) and transaction fees from the transactions included in the block.

