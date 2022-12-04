# Block

> ### `Description`
>
> Refers to computer files that store transaction data.  
> These blocks are arranged in a linear sequence that forms an endless chain of blocks - hence, the term blockchain.  
> Every newly generated block is connected to the previous one through the use of cryptographic techniques.

> ### `Genesis Block`
>
> The first ever block recorded on its respective blockchain network, also occasionally referred to as Block 0 or Block 1.
>
> When a block is broadcasted to the blockchain, it references the previous block. However, in the case of the genesis block, there is no previous block to reference.

> ### `Block Height`
>
> Represents the number of blocks that were confirmed in the entire history of a particular blockchain network - from the genesis block (or block zero) until the most recent one.  
> So the block height of the genesis block is #0, and the block height of the first block mined is #1.

> ### `Block Reward`
>
> Refers to the cryptocurrency rewarded to a miner when they successfully validate a new block
>
> Made of two components:
>
> - Block subsidy - newly generated coins and represents the biggest part of a block reward
> - Transaction fees - all fees paid by the transactions that are included in the block

> ### `Candidate Block`
>
> A block that a mining node (miner) is trying to mine in order to receive the block reward.
>
> So a candidate block may be described as a temporary block that will be either validated or discarded by the network
>
> Miners compete with each other to validate the next block and add it to the blockchain, but first, they have to create a candidate block to participate in the mining competition.
>
> Candidate blocks are created by miners by collecting and organizing multiple unconfirmed transactions from the memory pool.
>
> The root hash - together with the hash of the previous block and a random number called nonce - is then put into the block's header.The block header is then hashed by the miner, generating an output based on those components (root hash, previous block's hash, and nonce) plus a few other elements. The resulting output is the block hash and will serve as a unique identifier of the newly generated block (candidate block).
>
> To be deemed as valid, the output (block hash) must start with a certain number of zeros (less than a target value that is defined by the protocol). This means that the mining process is based on multiple attempts (trial and error) as the mining nodes have to perform a myriad of hashing functions with different nonce values until a valid block hash is eventually produced. The block hash produced is what proves that the miner did his work (hence Proof of Work).
>
> After a miner finds a valid block hash, their candidate block will be broadcasted to the rest of the nodes of the network, which will verify the authenticity of the hash. If everything is good, the candidate block will then be recorded into the blockchain. At this point, each validating node updates its copy of the blockchain data to reflect the recent mined block, and the miner will get the block reward.
