# Solidity Token
This Solidity program is a simple token creation contract that demonstrates the fundamental concepts and functionality of the Solidity programming language. It serves as an introductory example for those looking to understand token development on the Ethereum blockchain.

## Description
This program defines a basic token contract written in Solidity. The contract includes essential functions for minting (creating) and burning (destroying) tokens, along with public variables that store token details such as name, abbreviation, and total supply. This project serves as a foundation for developers who want to delve deeper into smart contract development.

## Getting Started
### Executing the Program
To run this program, you can use Remix, an online Solidity IDE. To get started, visit the Remix website at https://remix.ethereum.org/.

Create a New File: Click on the "+" icon in the left sidebar. Save the file with a .sol extension (e.g., MyToken.sol).

Copy and Paste the Code: Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract myToken {
    string public tokenName = "GENG";
    string public tokenAbbrv = "GG";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```
Compile the Code: Click on the "Solidity Compiler" tab in the left sidebar. Ensure that the compiler version is set to "0.8.18" (or another compatible version), then click on the "Compile MyToken.sol" button.

Deploy the Contract: Navigate to the "Deploy & Run Transactions" tab. Select the myToken contract from the dropdown menu, and click the "Deploy" button.

Interact with the Contract: Once deployed, you can use the mint and burn functions to manage the token supply. Input an address and a value, then click the corresponding button to execute the functions.

## Authors
Metacrafter Caps


## License
This project is licensed under the MIT License - see the LICENSE.md file for details.
