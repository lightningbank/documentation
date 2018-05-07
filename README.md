Lightning Network Documentation

World's Fastest Blockchain Platform Natively Implementing Bitcoin Lightning Network Protocol & Ethereum Plasma Framework

Lightning Root Blockchain

Building geth requires both a Go (version 1.7 or later) and a C compiler. You can install them using your favourite package manager. Once the dependencies are installed, run:

make all

Init Root Node

geth --datadir ./chaindata init ./Genesis.json

Start Root Node

geth --datadir ./chaindata --networkid 0 --port 30304 console 2>> bolt.log

Add Peer Node

In the geth JavaScript console of your root node, type:

> admin.addPeer(
"enode://2860c836b635b3b6ed84071a82735b749d47cc3994b2093d52867c354dee56dbdd49a5d7aa82aef1ef3ace5d82fdb776bfd9fbe0cd6e54dc2c1baf9e9e5ccda2@52.37.246.181:30303" )

> admin.addPeer(
""enode://1abefdca7cafaec401d443afcf86a0c08b1f8ea407895ae109c426c49f3ef058ff37259e7bc00574a0298aefbc376c0cacf2ffa3fd218f1506f9d7d5c63ecc58@52.35.28.8:30303"" )

> admin.peers

Create an Account

In the geth JavaScript console, create an account:

> personal.newAccount("<YOUR_PASSPHRASE>")

Set Default Account

Check your default account, type

> eth.coinbase

To set your default account, type 

> miner.setEtherbase(web3.eth.accounts[0])

Start mining

Check your balance with 

> eth.getBalance(eth.coinbase)

Run 

> miner.start()

To end mining, type 

> miner.stop()

