---
description: The Inner Machinations of the Blockchain
---

# How Blockchains Work

Let’s break down how blockchain actually works. As with technical concepts, it’s best to explain by example: we’ll walk you through the process which happens when a transaction is submitted to the blockchain.

## The Life of a Transaction

In the example, some technical jargon will be introduced, but worry not, they will be explained after.

Recall that blockchains ultimately are a tool for securely recording transactions. When transactions are submitted to the blockchain, the following processes occur:

1. A **block** is prepared, and ready to accept transactions for a specific time period.
2. During that time period, transactions are added to the block.
3. At the end of the time window, a **hash** is produced of all the transactions.
4. The block is digitally **signed** by the creator as a form of verification.
5. **Consensus** occurs, through which the validity and integrity of the block is verified across all blockchain network participants. If successful, the block is added to the blockchain, and the transactions are considered processed. The creator of the block is rewarded in the form of cryptocurrency for their service.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Simplified Illustration of How Blockchains Work. Source: Reddit u/steavus</p></figcaption></figure>

## Key Terms

There were a few key terms introduced there. Let’s break them down:

### Block

A block is an object which contains a batch of transactions which have occurred during a specific window of time. Each block is identified by the following:

* Body: contains the batch of transactions
* Block Header: contains unique identifiers, such as the information of the block and the block before it, who produced it, and when they were made

### Hash

A hash is a tamper-proof mechanism which maps an input value to a number of fixed-length. This serves as a unique identifier for a piece of content; changing the input changes the output. Here, it is used to produce a unique identifier of all the transactions in a block, and hence a unique identifier for the block itself.

In other words, it allows us to determine if a malicious actor tampers with the block’s transactions. Changing any transaction in a block will change the block body hash, thus changing the block’s header hash, the header hash of the next block, and so on, invalidating the entire chain that follows. This feature which prevents a blockchain to be tampered with is called **immutability**.

### Consensus

Consensus is the mechanism by which all network participants determine which transactions are valid, and the structure of the ledger. As a reward for expending computational resources to verify these transactions and producing blocks, the participants receive cryptocurrency. Depending on the specific blockchain this may be achieved through different mechanisms, but the two most popular ones are Proof-of-Work (PoW) and Proof-of-Stake (PoS).

<details>

<summary>Proof-of-Work</summary>

* In PoW, a node, also known as miner, solves a complex mathematical problem, or puzzle, to validate a transaction and add a new block to the blockchain. These puzzles are difficult to solve but easy to verify the correct solution.
* Once a miner has found the solution to the puzzle, they will be able to broadcast the block to the network where all the other miners will then verify that the solution is correct, and add the block to their copy of the blockchain. This process is called mining, and the miners receive a reward in cryptocurrency for their efforts.

#### Drawbacks

* One drawback of PoW is that it requires a lot of computational power to solve these puzzles, which can lead to high energy consumption and slower transaction speeds. As a result, some blockchain networks have implemented alternative consensus algorithms, such as Proof-of-Stake.

</details>

<details>

<summary>Proof-of-Stake</summary>

* PoS is another consensus algorithm used in blockchain networks, where nodes, or validators in this case, are selected to create new blocks based on the amount of cryptocurrency they hold and are willing to “stake”.
* This is like a group of people holding tickets to a lottery; the more tickets you have, the more likely you are to be chosen as the winner.
* In practice, there are a variety of PoS mechanisms which vary based on the blockchain network - some may require validators to lock up funds as collateral, others may use a delegation method where network participants can vote for validators by staking their cryptocurrency to them.

#### Advantages

* Unlike PoW, PoS does not require the nodes - called validators in this case - to solve complex, energy intensive mathematical puzzles to create new blocks.
* Additionally, PoS allows for faster transaction speeds as there is less contention to produce a block.

#### Drawbacks

* There is greater potential for centralization if a small number of validators hold a large amount of stake in the network.

</details>
