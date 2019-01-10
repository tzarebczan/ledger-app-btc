# Install LBRY
## Install BTC app and Install Ledger push tool
**Make sure BTC app is installed (use ledger manager) before proceeding.**

Install python and pip. Then run:
```pip install ledgerblue```

## Download app
Hex download: https://github.com/tzarebczan/ledger-app-btc/releases/tag/lbry
or compile: https://github.com/tzarebczan/blue-app-btc

## Install app
```python -m ledgerblue.loadApp --targetId 0x31100003 --tlv --apdu --fileName app.hex --appName LBRY --appFlags 0x00 --icon "0100000000ffffff00ffffffff7ffe1ff8cfe3e38ff83ffe9ff227c619184c63f38ffc3ffeffff"```

## Connect to Ledger:
If you have Electrum for BTC installed already, this will use the same directories (fix is in the works). So remove/backup those first. 

Choose Legacy address type. Enable manual fees. 

Windows exe: https://github.com/tzarebczan/electrum/releases/tag/0.0.1
or build from source
