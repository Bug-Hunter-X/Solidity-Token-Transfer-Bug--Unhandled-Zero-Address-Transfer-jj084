# Solidity Token Transfer Bug: Unhandled Zero Address Transfer

This repository demonstrates a common bug in Solidity smart contracts related to token transfers. The `transfer` function in the `bug.sol` file does not handle the case where the recipient address is the zero address (0x0000000000000000000000000000000000000000).  Transferring tokens to the zero address typically results in the loss of tokens, representing a significant security vulnerability.

The `bugSolution.sol` file provides a corrected version of the `transfer` function, addressing this vulnerability by including a `require` statement that reverts the transaction if the recipient address is invalid. This prevents the loss of tokens and enhances the security of the smart contract.

## How to Reproduce

1. Compile `bug.sol`.
2. Deploy the contract.
3. Attempt to transfer tokens to the zero address (0x0000000000000000000000000000000000000000).
4. Observe the transaction failing due to the lack of error handling.

## Solution

The `bugSolution.sol` file demonstrates the corrected implementation with proper error handling.