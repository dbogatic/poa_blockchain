#
# Proof of Authority (PoA) Blockchain 


The goal of this repo is to show steps needed to set up a testnet blockchain for an organization using Geth and to simulate a crypto transaction on the ETH network via MyCrypto application. To do this, we will need to:


* Set up a custom testnet blockchain using [Geth](https://geth.ethereum.org/).


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

    * We use the following two lines of code to setup Node1 and Node2 that will interact in our blockchain.

    * `./geth account new --datadir node1`
    * `./geth account new --datadir node2`

* ![NodeSetup](images/Screen_Shot7.png)

    Next, we initialize the nodes we created:

    * `./geth init dragancoin.json --datadir node1`

* ![Node1](images/Screen_Shot5.png)

    * `./geth init dragancoin.json --datadir node2`

* ![Node2](images/Screen_Shot6.png)

* Setup the Clique Proof of Authority consensus algorithm.

    * A consensus algorithm is a procedure through which all the peers of the Blockchain network reach a common agreement about the present state of the distributed ledger. [Source: Geeks for Geeks](https://www.geeksforgeeks.org/consensus-algorithms-in-blockchain/)

    * There are [three](https://www.geeksforgeeks.org/consensus-algorithms-in-blockchain/) consensus algorithms currently in use:
    
        * PoA (Proof of Authority) 
        * PoW (Proof of Work)
        * PoS (Proof of Stake)

    * In this case we will use PoA consensus algorithm which is setup once we initiated Node1 and Node2. 

    * The setup process includes selecting passwords for access to Node1 and Node2 as well as creation of Public and Secret keys, which are stored in the Keystore folder in each Node.

* ![PoA](images/Screen_Shot8.png)
Image Source:[Rice Bootcamp](https://rice.bootcampcontent.com/Rice-Coding-Bootcamp/rice-hou-fin-pt-09-2020)

    * You should keep the account Private Key always in a secure location and not allow access to it to anyone.

* ![keystore](images/Screen_Shot9.png)

    * The password we set in the above step for each Node we will use when we start the blockchain.

* ![password](images/Screen_Shot10.png)

#
### Send a Test Transaction
#



