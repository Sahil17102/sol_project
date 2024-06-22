# ETH PROOF: Beginner EVM Course
# Project Title
Write a contract by using of mapping,state variable make some function and get desired output.
## Description

 In this project we do that things:
 
 1. public variables storing details about dummy coin (Token Name, Token Abbrv., Total Supply).

 2. Mapping function [addresses to balances (address => uint)] .

 3. A mint function taking two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount
 
 4.  A burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.

 5.  Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned.

## Getting started
### Installing

* To run the project code, you need an IDE where you can run the Solidity language. One such IDE is the online Remix IDE (https://remix.ethereum.org/), which you can run on any browser of your choice.

* The code in this project can be used by simply copying it to the editor of any IDE where you can run Solidity version 0.8.7.
### Executing Program

How to run the program:

1.Copy the Solidity code provided in the "project_sol" file.

2.Open Remix IDE (https://remix.ethereum.org/).

3.In the Remix IDE, create a new file and paste the copied code into it.

4.Compile the Code by either pressing "Ctrl + S" to compile the code or using the Compile button in the Remix IDE interface.

5.Use the Deploy button in the Remix IDE to deploy the contract to a local Ethereum network or a test network.

 6. A mint function taking two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount

7.A burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.

8.Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned.


```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.7;
contract MyToken {

// public variables here
string public tokenName = "Token";
string public tokenAbbriv = "Tok";
uint256 public totalSupply = 0;

// mapping variable here
mapping (address => uint) public balances;

// mint function
function mint (address _address , uint256 _value) public {
   totalSupply += _value;
   balances[_address] += _value;
}
// burn function
function burn (address _address , uint256 _value) public {
   if (balances[_address] >= _value) {
   totalSupply -= _value;
   balances[_address] -= _value;
   }
}
}
```
## Help

If you encounter any issues or have any questions, here are some common solutions:

1. Ensure you are using Solidity version 0.8.7 or later.
   
2. Check the Remix IDE console for error messages and follow the guidance provided.

## Authors

Contributor name and info:

Sahil

gmail: sahilmittal1920@gmail.com

## License

 This project is licensed under the [MIT] License - see the LICENSE.md file for details.






