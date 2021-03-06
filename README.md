# ethtex-registry

Token registry smart contract for use by an exchange platform with on-chain settlement, in-order to allow token maps to be queried on-chain with minimal trust in any exchange operator. The implementation is write only.

Main contract can be found on `contracts/RegistryLookup.sol`

## Setup

Standard truffle project, so truffle should be installed globally, and regular cli commands can be used (`truffle compile`, `truffle migrate`, `truffle test`, etc)

## Seed

Example usage of the seed script:

```bash
node seed --provider "http://locahost:4321" --privatekey "potatos" --contract "0x123..." --token "0x111..." --token "0x222..." --token "0x333..."
```
or use shorthand alias:

```bash
node seed -p "http://locahost:4321" -k "potatos" -c "0x123..." -t "0x111..." -t "0x222..." -t "0x333..."
```


## Tests

Expect a provider to be present in `HTTP://127.0.0.1:8545` (like ganache) ( this can be changed on line 10 of `tests/RegistryLookup.spec.js`, and hardcoded private key on line 13).
