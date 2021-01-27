#
# Proof of Authority (PoA) Blockchain 


The goal of this repo is to show steps needed to set up a testnet blockchain for an organization using Geth and to simulate a crypto transaction on the ETH network via MyCrypto application. To do this, we will need to:


* Set up a custom testnet blockchain using [Geth](https://geth.ethereum.org/)


* Send a test transaction.

* Verify that test transaction was recorded in our blockchain and registered in our [MyCrypto](https://mycrypto.com/account) wallet.

#
### Setting up a Proof of Authority (PoA) Blockchain
#
In order to setup our testnet blockchain we will use:

* Puppeth, to name our network and generate the initial genesis block. THe following steps will acomplish this:

    * First, we name the network (in this case I named it dragoncoin)

    ![puppeth](images/Screen_Shot1.png)

    * Next, we configure the new genesis by sellecting a consensus algorithm (in our case we chose Proof of Authority).

    * We will also select accounts that will be included in the blockchain and decide if they should be prefunded.

    ![puppeth2](images/Screen_Shot2.png)

    * Lastly, we will set a custom network id (i chose a random number 670) and export our network (we can ignore the error messages because we only need files that were created to setup our Nodes)

    ![puppeth3](images/Screen_Shot3.png)
    ![puppeth4](images/Screen_Shot4.png)


* Geth, a command-line tool, to create keys, initialize nodes, and connect the nodes together.

    * We use the following two lines of code to initialize Node1 and Node2 that will interact in our blockchain.

    * `./geth account new --datadir node1`

* ![Node1](images/Screen_Shot5.png)

    * `./geth account new --datadir node2`

* ![Node2](images/Screen_Shot6.png)

* Setup the Clique Proof of Authority consensus algorithm.
#







