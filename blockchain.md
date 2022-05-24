# Blockchain

### Vocabulary :

- Bitcoin : The concept of Bitcoin or the entire network.
- bitcoin : a unit of currency of bitcoin, BTC or XBT
- bit : 1,000k bit == 1 BTC
- Block Chain : public record of Bitcoin transactions
- Block : record in block chain that contains and confirms many waiting transactions
- confirmation : transcation irreversible added to the block.
- cryptography : encrypts blockchain and adds security
- double spend : malicious user spending to two recipients at same time.
- Hash rate : measuring unit of processing power of Bitcoin, the network.
- Mining : Processing confirmations
- private key : allows to spend from a specific wallet
- Signature : provides ownership with private key sign
- Wallet : contains private key and record of BTC owned

Learning Outcomes :
    - Explain 3 fundamental characteristics that define blockchain
    - Important features of Ethereum blockchain
    - Algo and techniques that enable a blockchain : crypto and hashing
    - outline methods for realizing trust in a blockchain

## Week 1 : Blockchained Defined

### Blockchain

- ConsenSys : John Wolpert
    - Largest blockchain company
    - based on Wash DC
    - New Venture development lab
    - blockchain : nimble procerious route for transaction

### Bitcoin and Blockchain
    - Blockchain :
        - p2p transaction of digital asset without intermediatry
        - user cases : Goods transfer, Media transfer, Platform for decentralised business logic, distributed resources, crowd operation and fundings
        - democratic approach
    - Bitcoin :
        - continuous working digital currency
        - Autonomous decentralized application
        - Satoshi Nakamoto : creator of TBC
    - Blockchain :
        - Software program for Validation, Verification and consensus
        - P2P transcation in decentralized network
        - Establisihing trust among peers
        - Recording transactions in distributed ledger
    Establishing trust :
        - Have a process in place to validate, verify and confirm transcations and can be done by :
            - Record transaction in a ledger
            - record the transaction in distributed ledger of blocks
            - create a tamper-proof record of chains of blocsl.
            - implement a conensus protocol to add to the chain 
        - Provides us with : Validation, verification, consensus and immutable recording.

### Blockchain Structure :

- transaction - block - chain
- consensus process used to add block. Verified my miners.
- basic unit : UTXO : Unspend transaction output
- Set of all UTXO defines the state of the Bitcoin blockchain
- Role
    Transaction : uses amount specified to input UTXO to output UTXO based on consensis specified. 
- UTXO Structure : 
    - Unique ID of the transaction created by UTXO
    - its index in output list
    - value/amount its good for
    - optional contract
- Transaction Structure :
    - Ref No of transaction
    - 1 or more input and output UTXOs
    - total input and output amount
- Trust :
    - Participants can validate the transactions
    - Validation and verification methods defined by the blockchain and implemented by peers provide trust in DeSys.

### Basic Operations
    - Validation of transactions
        - input UTXOs are valid
        - output UTXOs are correct
        - IO amounts match
        - reject if conditions wrong
        - creates a block if conditions met
    - Gathering transactions for a block 
    - Broadcasting valid transactions and block
    - Consensus on next block creation
    - chaining blocks

    Miners compete to validate a transaction and broadcast the completed block, other participants verify the block and reach a consensus to add a new block to the chain.
    Algo for consensus is Proof-of-work protocol
    Minors fee is the index 0 of the block, also called coinbase transaction. Miners fee is 12.5 BTC for a bitcoin. (Need to confirm)

### Beyond Bitcoin
    Three Types of Blockchain 
        Type 1 : Only Cryptocurrency, TBC
        Type 2 : Currency + Business Logic, ETH
        Type 3 : Only Business Logic, HyperLedger

    Blockchain Category based on access limits
        - Public : Open to internet
        - Private : Only allowed collaborators
        - Permissioned : Consortium blockchain for ease of governance, provenance and accountability.

## Week 2 : Ethereum Blockchian

Objectives :
    - Discuss smart contract
    - illustrate Ethereum Blockchain protocol, elements and operations
    - Demonstrate concept of "gas"
    - incentive model of eth

### Smart Contracts in Ethereum

    - Piece of code in the node
    - ETH can do complicated transfer with conditional transfers
    - Smart contract resemebles class object in OOPs
    - EVM : Ethereum Virtual Machine. Provide a platform independent computational platform
    - node Smart contact in Solidity -> compiled to Byte code -> executed in EVM

### Ethereum Structure
    - ETH have accounds 
        EOA : Externally owned accounts are controlled by Private keys. Need to participate on ETH
        CA : Contract Accounts or smart contract accounts are controlled by the code and activated only by a EOA
    Interact with Blockchain with transactions, every account have a coin balance.
    Fees are paid in Wei. 1 ETH = 10^8 Wei
    
### Ethereum Operations

 - ETH Node has software needed for transaction initiation, validation, mining block creation, SC execution and EVM.
 - SC is designed, developed, compiled and deployed on the EVM.
 - Currency state of SC is the values of variables defined in it.
 - A BC maintian state has and receopt has.
 - Transaction validation involves checking the time-stamp and nonce combination to be valid and availablibity of fees
 - Concensus protocol used is memory-based than a CPU based proof of work.

### Incentive Model

    - Mining secures the network
    - ETH uses incentive based model for block creation
    - Gas points are used measure the fee of computation
    - Gas points is independent of crypto market and does not swing with fluctuations in ETH value
    - Gas limit : amount of gasl points available to spend
    - The number of transactions and complexity of smart contracts are restricted by block gas limit
    - Gas Spend : amount of gas spend at the completion of the block creation.
    
    Mining Incentive Model 
    - Proof of work winner miner will create a new block that will be added to the chain
        - 3 ETH and transaction fees.
        - Gets Gas Points
    - Other minors who also computed the transaction but did not make it to the block is called Ommers.
        - Blocks created is called Ommer Blocks
        - Gets a percentage of total gas points as a consolation and network security

## Week 3 : Algo and Techniques

### Public key Cryptography

### Hashing

### Transactional Integrity

### Securing Blockchain

## Week 4 : Trust Essential

### Decentralized Systems

### Consensus Protocol

### Robustness

### Forks


## Abbrevations 

DeSys : Decentralized System
DeNet : Decentralized network
DeFi : Decentralized Finance