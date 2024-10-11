README FILE FOR BLOCKCHAIN IMPLEMENTATION
    
INSTRUCTIONS FOR RUNNING THE NODES:
      1. Initially, Node 1 has 100000 coins, which can be sent to other accounts.
      
      2. The nodes are activated using client.py file using : "python3 client.py Receive"
      
      3. In order to create a transaction, create another instance of client.py, the previous Receive must remain active. Now, to send money use: "python3 client.py Send "receiver's address" value to be sent(e.g., 12.0) fees(e.g., 3.0)"
      
      4. In order to mine a block, use: "python3 client.py Mine"
      
      5. Each node uses three types of messages to send peer info, transactions and blocks to every other node. For e.g. :-
                             1 - peer_add,
                             2 - new transaction received,
                             3 - new block received
                             
      6. Once a block has been verified, it is stored in the main "BKS" folder.
      
      7. A node that runs for the first time creates a dict of various keys and stores them in an encrypted file protected by user-provided password. This password is needed to perform any operation on this node.
      
      8. In order to create a new node, run "./node_gen.sh n", which creates a folder "Noden", n could be any non-existent node(integer number). During the first run, the key file is created and stored.
      
      
MAIN FILES FOR NODES:
      1. bks.py - defines Block class
      2. txs.py - defines Transaction Class
      3. utils.py - defines merkle_tree functions
      4. gen_keys.py - generate a dict of keys for each node.
      5. node.py - contains the Node  class
      6. client.py - provides the command line functionalities for each node.
      7. genesis.json - the first block of this blockchain. Node1 gets 100000 coins in this block.
      8. UTXO.json - contains the transaction output in genesis block.
      
     
FURTHER PLANNED ADDITIONS:
      1. Support for dynamic mining - increasing and decreasing the difficulty for the same.
      2. Creating lightweight SPV(Simple Payment Verification) Nodes"
      3. Support for concurrent mining and fork chain.
      4. Implementing a wallet for every account(GUIs if possible).
      
      
