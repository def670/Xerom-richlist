# The Xerom Richlist

This project is based off Ether1 project (https://ether1.org) Richlist.  This release is tuned for Xerom

## 1. Richlist

This is the Richlist for the Xerom project. It works by building the DB from the blockchain, going block by block and processing transactions for each block.
You can read more about it [here](https://github.com/taeguscromis/etho/tree/master/richlist)

![Richlist showcasw](https://github.com/def670/Xerom-richlist/blob/master/Xerom-richlist.png)


1. Modules
Xero geth daemon with rcp - can be installed like this: wget -N https://github.com/xero-official/go-xerom/releases/download/2.1.0/geth-linux.zip
chainsync module (EtherSync)
webfront module (PHP page)

2. Xero geth daemon 
In order for richlist to work it needs the data from the etho geth RPC. You can either use remote RPC node or you can install local geth and use that. Local geth is recomended for the speed. If you do that however be sure that the chain is synced before starting the EtherSync module.

3. Chainsync (EtherSync) module
This is the module that processes the transactions from the blockchain and stores them in the local mysql DB. It also calculates the data for the richlist. It must run as system service. How to set it up is described here.

4. Webfront module (PHP page)
This is the user interface, the fronend web page. Its a simple PHP web page that gets data from the mysql DB. How to set it up is described here.
