# NativeCoin (NTVCN) - Simple ERC20 Token

NativeCoin (NTVCN) is a simple ERC20 token smart contract implemented in Solidity. This contract allows you to create and manage your own 
ERC20 token with basic functionalities like minting and burning tokens.

## Description

The NativeCoin contract is a basic implementation of an ERC20 token. It provides the following functionalities:
1. Minting: The contract allows the creation of new tokens by calling the mint function. When called, 
this function increases the total supply of NativeCoin by the specified amount and also adds the same amount of tokens to the balance of the sender's address.
2. Burning: The contract also allows burning (destroying) tokens by calling the burn function. This function decreases the total supply of NativeCoin by the
specified amount and deducts the same amount of tokens from the balance of the sender's address.

## Getting Started

To get started with using the NativeCoin (NTVCN) token contract, follow the instructions below:

### Installing

You don't need to install anything for this smart contract. It will be deployed on the Ethereum blockchain.

### Executing program

To interact with the NativeCoin (NTVCN) smart contract, you can use Ethereum wallets or web3 libraries 
with your preferred programming language. Here are the step-by-step instructions:
1. Deploy the contract on the Ethereum network using a development environment or any Ethereum wallet that supports smart contract deployment.
2. Once the contract is deployed, you can start minting new tokens by calling the mint function, providing the recipient's address and the amount of tokens to mint.
3. To burn tokens, use the burn function, passing the recipient's address and the number of tokens to burn. The function will check if the sender has a sufficient balance before burning tokens.
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "NATIVECOIN";
    string public tokenAbbrv = "NTVCN";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint (address add, uint val)public {
        totalSupply += val;
        balances[add] += val;
    }

    // burn function
    function burn (address add, uint val)public {
        if (balances[add] >= val){
            totalSupply -= val;
            balances[add] -= val;
        }
    }

}
```

## Help

If you encounter any issues or have questions related to the NativeCoin (NTVCN) token contract, 
please feel free to reach out to the contract creator or refer to the official Solidity documentation.


## Authors

Contributors names and contact info

Danz Andrew Permejo
@danzpermejo(https://github.com/danzpermejo)


## License

This contract is released under the MIT License.
