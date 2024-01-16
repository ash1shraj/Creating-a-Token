# MyToken Smart Contract

## Overview

This repository contains a simple Ethereum-based smart contract written in Solidity, a programming language specifically designed for creating smart contracts on the Ethereum blockchain. The contract, named `MyToken`, represents a basic token implementation with functionalities for minting and burning tokens.

## Contract Details

### Variables

- `tokenName`: A public variable representing the name of the token.
- `tokenSymbol`: A public variable representing the symbol of the token.
- `totalSupply`: A public variable representing the total supply of the token.
- `balances`: A mapping that associates Ethereum addresses with their respective token balances.

### Constructor

The contract has a constructor that initializes the `tokenName` and `tokenSymbol` when the contract is deployed.

```solidity
constructor(string memory _name, string memory _symbol) {
    tokenName = _name;
    tokenSymbol = _symbol;
}
```

### Minting Function

The `mint` function allows the creation of new tokens and assigns them to a specified Ethereum address.

```solidity
function mint(address _address, uint256 _value) public {
    totalSupply += _value;
    balances[_address] += _value;
}
```

### Burning Function

The `burn` function reduces the total supply and the balance of a specific address by a specified amount.

```solidity
function burn(address _address, uint256 _value) public {
    require(balances[_address] >= _value, "Insufficient balance");
    totalSupply -= _value;
    balances[_address] -= _value;
}
