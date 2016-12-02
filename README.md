# bitcoinlib
Bitcoin library with key manipulation function to generate, import and convert cryptograpic keys.

Implements BIP0032, BIP0039, BIP0033 and BIP0044
 

## Usage Example's

#### Generate random Private Key
```python
from bitcoinlib.keys import *
k = Key()
print k.info()
```

#### Import Private Key (WIF format)
```python
privatekey_wif = 'L3RyKcjp8kzdJ6rhGhTC5bXWEYnC2eL3b1vrZoduXMht6m9MQeHy'
k = Key(privatekey_wif)
print k.info()
```
 
#### Show public key and bitcoin address
```python
print k.public()
print k.get_address()
```

#### Requirements
* ecdsa
* pbkdf2
* pycrypto
* scrypt
* binascii

$ sudo apt install python-dev python3-dev
To install OpenSSL development package on Debian, Ubuntu or their derivatives:
$ sudo apt-get install libssl-dev

To install OpenSSL development package on Fedora, CentOS or RHEL:
$ sudo yum install openssl-devel