# IPFS & standards for encrypted data 

### TERMS

DID - Decentralized identifiers - specifies a general way of going from a string identifier, e.g. did:3:bafy.. to a did document including public keys for sig verification

IPLD - interplanetary linked data - data model for interoperable protocols

JOSE - JSON object signing and encryption using CBOR

CBOR - Concise Binary Objject Representation - binary data serialization format loosely based on JSON

JWE - JSON web encryption

signature - signed to prove who the author is

multiformats - Interface for multihash, multicodec, multibase and CID

Provider (context: ethers) - provides abstraction for a connection to the Ethereum network
Signer (context: ethers) - directly or indirectly has access to a private key which can sign transactions to authorize the network to charge your account ether to perform ops


### BUILDING BLOCKS 

ipfs-core

js-3id-did-provider - did provider used within 3ID Connect to connect with eth wallet

key-did-provider-ed25519 - EIP-2844 impl. simple DID provider that supports both signing and encryption - RECOMMENDED PROVIDER

js-did - represent user in form of a did - encrypt datta and store directly on ipfs

dag-cbor - encoding (in background)

3ID Connect generates necessary authentication secrets


DAGJWS - signed but not encrypted
- setup DID instance using provider
- create a signed data structure
- add data
- make a signed data object


DAGJWE - Encrypted data object
- IPLD data object encrypted to one or many DIDs -> stored directly on ipfs
- DID can be the user itself but also other chosen users
- decrypt

### ARCHITECTURE / FLOW

Create the EthereumAuthProvider(3ID) or alternative solution - connect wallet

Get the DID provider from the 3ID Connect instance

create DID session/authenticate did

create DAGJWE and add to IPFS


### LINKS

https://blog.ceramic.network/how-to-store-signed-and-encrypted-data-on-ipfs/

