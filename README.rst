.. image:: https://travis-ci.org/spesmilo/electrumx.svg?branch=master
    :target: https://travis-ci.org/spesmilo/electrumx
.. image:: https://coveralls.io/repos/github/spesmilo/electrumx/badge.svg
    :target: https://coveralls.io/github/spesmilo/electrumx

===============================================
ElectrumX - Reimplementation of electrum-server
===============================================

  :Licence: MIT
  :Language: Python (>= 3.8)
  :Original Author: Neil Booth

This project is a fork of `kyuupichan/electrumx <https://github.com/kyuupichan/electrumx>`_.
The original author dropped support for Bitcoin, which we intend to keep.

ElectrumX allows users to run their own Electrum server. It connects to your
full node and indexes the blockchain, allowing efficient querying of the history of
arbitrary addresses. The server can be exposed publicly, and joined to the public network
of servers via peer discovery. As of May 2020, a significant chunk of the public
Electrum server network runs ElectrumX.

Documentation
=============

See `readthedocs <https://electrumx-spesmilo.readthedocs.io/>`_.


What I did
=================
change rpc_query result type from [str] to json
   :Query RPC: root@localhost:~/electrumx# ./electrumx_rpc query 1EHNa6Q4Jz2uvNExL497mE43ikXhwF6kZm 1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH bc1qw508d6qejxtdg4y5r3zarvary0c5xw7kv8f3t4 3JvL6Ymt8MVWiCNHC7oWU6nLeHNJKLZGLN
   :RPC Result: {'1EHNa6Q4Jz2uvNExL497mE43ikXhwF6kZm': {'type': 'address', 'address': '1EHNa6Q4Jz2uvNExL497mE43ikXhwF6kZm', 'transactions': [{'n': 0, 'height': 144068, 'tx_hash': 'd61aa2a5f5bce59d2a57447134f7ce9ce9d29b5c471f4bf747c43bf82aa26c2a'}, {'n': 1, 'height': 144069, 'tx_hash': '06ce5606e4f0aaf8627b37326b386a5dab29f3c661fe464b9e99574fd04f38b9'}, {'n': 2, 'height': 147791, 'tx_hash': '16b3e640db786914b5021321aad4366ea4361e2eaeb0ac0ae1cc78f639463d81'}, {'n': 3, 'height': 147850, 'tx_hash': 'c727c06844ba74300f79e9cc0357fce4ebd1017ecec96bb25b0232d4a0e315ee'}, {'n': 4, 'height': 147856, 'tx_hash': '312fe3442a4668444a885260cf27037617cb258c30fd2724b410af1390e4f1d6'}, {'n': 5, 'height': 147856, 'tx_hash': '53033f758d085791267ea0e1b715932fb63f67bbb02cabd1bb354443adfb6a3e'}, {'n': 6, 'height': 162917, 'tx_hash': '9dc508dc7aa1965f9d7441239a752c3b443a849040ce2bba04a7a7dbb3f8c375'}, {'n': 7, 'height': 162926, 'tx_hash': 'b25f223208d33e8c4920677d0fe4056600188ef54d8060cf516e5768da4c10b6'}], 'utxos': [], 'balance': 0.0}, '1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH': {'type': 'address', 'address': '1BgGZ9tcN4rm9KBzDn7KprQz87SZ26SAMH', 'transactions': [], 'utxos': [], 'balance': 0.0}, '3JvL6Ymt8MVWiCNHC7oWU6nLeHNJKLZGLN': {'type': 'address', 'address': '3JvL6Ymt8MVWiCNHC7oWU6nLeHNJKLZGLN', 'transactions': [], 'utxos': [], 'balance': 0.0}}
