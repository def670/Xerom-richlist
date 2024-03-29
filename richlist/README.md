## 1. Modules

- Xerom geth daemon with rcp
- chainsync module (EtherSync)
- webfront module (PHP page)

## 2. Xerom geth daemon

In order for richlist to work it needs the data from the xerom geth RPC. You can either use remote RPC node or you can install local geth and use that. Local geth is recomended for the speed. If you do that however be sure that the chain is synced before starting the EtherSync module. For our instance using Xerom you can get geth like this:

**wget -N https://github.com/xero-official/go-xerom/releases/download/2.1.0/geth-linux.zip**

## 3. Chainsync (EtherSync) module

This is the module that processes the transactions from the blockchain and stores them in the local mysql DB. It also calculates the data for the richlist. It must run as system service. How to set it up is described [here](https://github.com/def670/Xerom-richlist/blob/master/richlist/chainsync/).

## 4. Webfront module (PHP page)

This is the user interface, the fronend web page. Its a simple PHP web page that gets data from the mysql DB. How to set it up is described [here](https://github.com/def670/Xerom-richlist/tree/master/richlist/webfront).
