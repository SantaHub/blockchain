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
    Learning Objectives :
        - summerize Public key cryptography
        - Secure Hashing and Merkle Tree hashing
        - Application of hashing and cryptography in protecting the blockchain

### Public key Cryptography
    Symmetric key Encryption : Same key is used to encrypt and decrypt the message
        - Easy to derive the secret key from encrypted data
        - Key transaction
    Public key cryptography : RSA Algorithm
        - Use a key pair to encrypt with public key and decrypt using private key
    Elliptice curve cryptohraphy ECC : 
        - Bitcoin and Ethereum for generating a key pair.
    256 bits ECC key pair ~= 3072 bits RSA key pair.

### Hashing
    converts arbitary length of value to a fixed length of values using a key
    Features :
        - Hashing algo should be one-way function
        - Collision Free
    Common algos :
        - SHA-3
        - SHA-256
        - Keccak-256
    common size is 256 bit
    Hashing is used to generate :
        - Account addresses
        - Digital Signature
        - Transaction hash
        - state hash
        - receipt hash
        - block header hash
    
### Transaction Integrity

    - Secure and unique account address
        1. 256 bit random number generated for private key
        2. ECC algo applied to private key to generate public key
        3. Hashing applied to pubilc key to obtain account address
    - Authorization of the transaction by the sender thorugh digital signing 
        - Authorized 
        - non - reputatble
        - unmodifiable
    - Verification of content not altered.

    1. Find the hash of the data fields of the transaction
    2. Encrypt the hash using the private key of the participant originating the transaction
    3. Hash is added to the transaction

    Complete transaction verification, also verify :
        - timestamp
        - nounce
        - account balance
        - available of fees

### Securing Blockchain

    Main components of the ETH block :
    - Block Header
    - Transaction hash and root
    - State Hash and root

    Integrity of a block

    - Block header contents not tampered with
    - Transactions are not tampered with
    - State transitions are computed, hashed and verified

    Block hash is the hash of all elements in the header, keccak is used to hash.
    A bitcoin block have 2000 transactions and ETH block have 100 transactions

    Hashes in a block are computed in a tree structure called merkle tree hash.
    Merkle TH is also used to hash state root since only the hash of chained state from block to block has to be recomputed.
    
    You dont have to go through the entire set of transactions. Smart Contract executuon in ETH result in state transition. Every state change requries state root re-computation.

## Week 4 : Trust Essential

Learning Outcomes :
    - Define elements of trust in a blockchain
    - Discuss consensus protocol
    - Explain Trust
    - Illustrate soft fork and hard fork

### Decentralized Systems

    -  Secure chain using protocols
    - validate transaction and block
    - Verify availability of resources
    - Executing and confirming transactions

    Trust Trail :
        - Valid Tx
        - Verify gas and resources
        - Execute Tx to get to a new state
        - Form new block
        - Come to a consensus
        - Add block to chain

### Consensus Protocol

 Proof-of-work is used to select the next block in blockchain
    - uses hashing
 Proof-of-stake is also debated as a consensus protocol.

### Robustness

 When consensus happen at same time, blockchain do chain split and wait for next transaction to be completed. The second consensus completion happening at same time is of low probability and that chain will get consolidated into the main chain over the other.
 ETH allows ommer blocks and provide a small incentive.
 Double spending : same input Tx referenced multiple times.
 Double spending is handled in TBC by considering the timestamps and acknowledging only the oldest transaction.
 ETH uses account number and global nonce is used. The timestamp and unique nonce is validated to avoid double spend.

### Forks

Forks Allows Blockchains to make changes in their underlying systems and version updates, the emerging two chains could be incompatible.
Forks can build credibility to chain.
Soft forks are minor changes to the system

## Abbrevations 

DeSys : Decentralized System
DeNet : Decentralized network
DeFi : Decentralized Finance