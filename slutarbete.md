#IPFS & standards for encrypted data 

### TERMS

DID - Decentralized identifiers - specifies a general way of going from a string identifier, e.g. did:3:bafy.. to a did document including public keys for sig verification

IPLD - interplanetary linked data - data model for interoperable protocols

JOSE - JSON object signing and encryption






### Building blocks

ipfs-core

js-3id-did-provider - did provider used within 3ID Connect to connect with eth wallet

key-did-provider-ed25519 - EIP-2844 impl. simple DID provider that supports both signing and encryption

js-did - represent user in form of a did - encrypt datta and store directly on ipfs

dag-cbor - encoding (in background)


### ARCHITECTURE

DAGJWS - signed but not encrypted
> setup DID instance using provider
> create a signed data structure
> add data
> make a signed data object


DAGJWE - Encrypted data object
> IPLD data object encrypted to one or many DIDs -> stored directly on ipfs
> DID can be the user itself but also other chosen users
> decrypt



### LINKS

https://blog.ceramic.network/how-to-store-signed-and-encrypted-data-on-ipfs/
