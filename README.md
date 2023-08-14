# Solidity Token

This Solidity program is a simple smart contract to create your own token as well as mint and burn the same.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. In this program , we have declared all the variables and mapped addresses to balances . We have also declared two functions which adds the tokens and removes the token from the balance and the total supply.
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., firsttoken.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.10;
contract MyTokenBones {

    // public variables here
    string public tokenname="Bones";
    string public tokenabbrv="BNS";
    uint public totalsupply=10;
    // mapping variable here
    mapping(address => uint)public balance;
    // mint function
    function mint(address recepientaddr, uint _tokens)public {
      totalsupply += _tokens;
      balance[recepientaddr] += _tokens;
   }
    // burn function
   function burn(address receipientaddr, uint _tokens)public {
      if(balance[receipientaddr]>= _tokens){
        totalsupply -= _tokens;
        balance[receipientaddr] -= _tokens;
      }
     }
  }

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.10" (or another compatible version), and then click on the "Compile firsttoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "firsttoken" contract from the dropdown menu, and then click on the "Deploy" button.

Then you can either mint(add) or burn(deduct) from the balance and total supply by clicking on transact after entering the required inputs.

## Authors

Praneel Patel  
[@praneelpatel88@gmail.com]


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
