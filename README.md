# Install LBRY
## Install BTC app and Install Ledger push tool
**Make sure BTC app is installed (use ledger manager) before proceeding. BTC app upgrades may require update of LBRY app too**

Install python (2.x or 3.x) and pip. Windows pip instructions:https://www.liquidweb.com/kb/install-pip-windows/

Then run:
```pip install ledgerblue```

## Download app
Hex download: https://github.com/tzarebczan/ledger-app-btc/releases/tag/lbry
or [compile](https://www.reddit.com/r/tezos/comments/8xf9ge/compiling_the_tezos_ledger_nano_s_app/): https://github.com/tzarebczan/ledger-app-btc - ```make COIN=lbry```

## Install app
```python -m ledgerblue.loadApp --targetId 0x31100004 --tlv --apdu --fileName lbry.hex --appName LBRY --appFlags 0x00 --icon "0100000000ffffff00ffffffff7ffe1ff8cfe3e38ff83ffe9ff227c619184c63f38ffc3ffeffff"```

## Remove app (on upgrade)
```python -m ledgerblue.deleteApp --appName LBRY --targetId 0x31100004```

## Connect to Ledger:
If you have Electrum for BTC installed already, this will use the same directories (fix is in the works). So remove/backup those first. 

Windows exe: https://github.com/tzarebczan/electrum/releases/tag/0.0.1
or build from source

Choose Legacy address type. Enable manual fees. 
