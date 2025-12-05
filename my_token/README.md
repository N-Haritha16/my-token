MyToken (MTK)
Overview

MyToken (MTK) is a simple ERC-20 compatible token built on Ethereum for learning and experimentation purposes.
This project demonstrates the standard functionalities of an ERC-20 token.

Token Details

Name: MyToken

Symbol: MTK

Decimals: 18

Total Supply: 1,000,000 MTK

Features

✅ Standard ERC-20 implementation

✅ Transfer tokens between addresses

✅ Approve and transferFrom functionality

✅ Event emission for transparency

✅ Balance tracking

Solidity Contract
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply * (10 ** decimals()));
    }
}


Notes:

Uses OpenZeppelin ERC-20 implementation for security.

initialSupply should be provided in whole tokens; decimals are automatically handled.

How to Deploy

Open Remix IDE

Create a new file named MyToken.sol and paste the contract code.

Compile the contract with Solidity 0.8.x.

Go to the Deploy & Run tab, choose your environment (e.g., Injected Web3 for MetaMask).

Deploy the contract by specifying the initial supply (e.g., 1000000 for 1,000,000 MTK).

How to Use
Check Balance
let balance = await myToken.balanceOf(userAddress);
console.log(balance.toString());

Transfer Tokens
await myToken.transfer(recipientAddress, 100 * (10 ** 18));

Approve and Transfer From
await myToken.approve(spenderAddress, 500 * (10 ** 18));
await myToken.transferFrom(ownerAddress, recipientAddress, 500 * (10 ** 18));

References

OpenZeppelin ERC-20 Documentation

Ethereum ERC-20 Standard

Remix IDE