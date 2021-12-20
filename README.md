# Metamac Blockchain
I have created a new network called the *Metamac* Blockchain<br/>
I have created 2 nodes for the Metamac network<br/>
- Node 1: 0xF6C41d2695c713Ea21973353D1E866D240613fdb
- Node 2: 0xD33A1Eef3425a74105D36c6BABfB96a1AdD853b0

## Puppeth Config
<br/>![](./screenshots/puppeth_config1.png)
![](./screenshots/puppeth_config2.png) <br/>

## Initialize Each Node
<br/>![](./screenshots/initialize_nodes.png)<br/>

## Enable Mining and RPC flag for Node1
<br/>![](./screenshots/rpc_enabled.png)<br/>

## Enable Peer Port for Node2
<br/>![](./screenshots/peerport_node2.png)<br/>

## Test Transaction
<br/>![](./screenshots/transaction_transfer.png)<br/>

## Transaction Hash
<br/>![](./screenshots/transaction_hash.png)<br/>

# Documentaion for ZBank's Private Testnet of *Metamac Blockchain*

To set up the Metamac testnet you will need to use the following skills & tools:<br/>
- Use *Puppeth* to generate your genesis block.
- Use *Geth* (a command line tool) to create keys, initialize nodes, and connect the nodes together.
- Use *Clique* as the Proof of Authority Algorithm.

## *To Run & Connect the Nodes*
Note: Run the Nodes in separate terminal windows with the commands:
### Node1
- ./geth --datadir node1 --unlock "0xF6C41d2695c713Ea21973353D1E866D240613fdb" --mine --rpc --allow-insecure-unlock
### Node2
- ./geth --datadir node2 --unlock "0xD33A1Eef3425a74105D36c6BABfB96a1AdD853b0" --mine --port 30304 --bootnodes "enode://9972693da61f7da52757801f15cb28d8c920de3c4af06c96c7232f6d363aa3e4828735649054f5cb64422d6624846caabaebb4432f665821909e76d4979f3295@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock<br/>
NOTE: Type your password and hit enter - even if you can't see it visually!

*Your Private PoA Metamac Blockchain should be now up and running.*
## *To Send Transactions Using METAMASK*
Setup METAMASK Wallet with a Custom Network using the following settings:<br/>
<br/>![](./screenshots/metamask_network.png)<br/>

Make sure you are using the same Chain ID as before and using ETH as the currency.

Import both *Keystore* files for Nodes 1 & 2 from the "node1/keystore" directory as follows:<br/>
<br/>![](./screenshots/keystore.png)<br/>
    
### *You may now send a Transactions from the Node1 account to the Node2 account*
<br/>![](./screenshots/transaction_transfer.png)<br/>