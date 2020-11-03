# Money Moves!!
Creating Ethereum based currency with Blockchain- proof of authority

## INITIATED NODE 1 AND NODE 2

1. Create accounts for two nodes for the network with a separate datadir for each using geth.

./geth --datadir node1 account new
./geth --datadir node2 account new

2. Run the nodes in separate terminal windows with the commands:

./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock
./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

![alt text](https://github.com/natyrrr/Money_moves/blob/main/Screenshots-process/initiated%20nodes.png)


## CREATED A GENESIS BLOCK

1. Open a terminal window, navigate to the Blockchain-Tools folder and type the following command:

./puppeth

2. Type in a name for your network, banknote for mine and hit enter to move forward in the wizard.


Type 2 to pick the Configure new genesis option, then 1 to Create new genesis from scratch:

3. Now you have the option to pick a consensus engine (algorithm) to use.

Type 1 to choose Proof of Authority and continue.

enter addresses for node 1 and node 2.

You will be asked to enter a pre-fund account and choose no


Copy and paste an address from your Ethereum wallet in MyCrypto, without the 0x prefix.


Once you paste an address and hit enter, hit enter again on the blank 0x address to continue the prompt.


Continue with the default option for the prompt that asks Should the precompile-addresses (0x1 .. 0xff) be pre-funded with 1 wei? by hitting enter again,
until you reach the Chain ID prompt.

4. Choose a chain ID.

5. download network json files.

![alt text](https://github.com/natyrrr/Money_moves/blob/main/Screenshots-process/created%20genesis%20block.png)


## INITIATED MINING NODE 1


1. Initiared mining on node 1 using:
./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock


![alt text](https://github.com/natyrrr/Money_moves/blob/main/Screenshots-process/MINING%20NODE%201.png)


## INITIATED MINING NODE 2

1. Initiated mining in node 2 using:
./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock


![alt text](https://github.com/natyrrr/Money_moves/blob/main/Screenshots-process/MINING%20NODE%202.png)

## ADDED KEYSTONE FILE AND CONNECTED BANKNOTE TO MY CRYPTO WALLET

1. logged into MyCrypto.
2. changed my network by creating a custom network using the network created using the genesis block. (banknote)
3. after connected I added a keystone file and was able to confirm my mining amount were in my wallet.

![alt text](https://github.com/natyrrr/Money_moves/blob/main/Screenshots-process/CONNECTED%20NETWORK%20TO%20MYCRYPTO.png)


## SENDING MONEY TO MYSELF

1. sent myself some money to confirm the transaction.
2. SUCCESS!!

![alt text](https://github.com/natyrrr/Money_moves/blob/main/Screenshots-process/SENDING%20MONEY%20TO%20MYSELF.png)




