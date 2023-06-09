# My Token
This Solidity project's main objective is to construct a token contract that enables users to create and burn tokens. Conditional expressions are also used by the software to ensure that specific actions are only taken when they can be completed. It also makes it possible to track balances associated with certain addresses.


# Description
This application is a simple contract that counts the number of tokens owned by each address using a mapping data structure. The program offers two operations: one to add tokens and the other to delete them. Overall, this program serves as a helpful simulation, illuminating the creation and destruction of tokens.


# Getting Started
Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:


    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;
    contract MyToken {
    // public variables here
    string public TokenName = "Coin";
    string public TokenAbbrv = "Eth";
    uint public  TotalSupply = 0;

    /// mapping variable here
    mapping(address => uint) public balances;
     
    // mint function
    function mint (address _address, uint _value) public {
       TotalSupply += _value;
       balances[_address] += _value;
    }
    
    // burn function
    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
          TotalSupply -= _value;
          balances[_address] -= _value;
       }
    }
    }
    
    
  To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

To deploy the contract, click on the "Deploy and Run Transactions" button. This will open a new window that allows you to deploy the contract. Do not forget to select the “MyToken” contract before deploying.

In the deployment window “Deployed Contracts”, set the parameters for the balance, mint, and burn functions.

* To mint new tokens, input the address of the recipient and the number of tokens you want to mint and click transact.
* To burn tokens, input the address of the recipient and the number of tokens you want to burn and click transact.
* To see current balances of the address, input the address of the recipient and the number of tokens you want to mint and click call. You can also see the total supply by clicking the “totalSupply” button.


# Authors
NTCIAN Aljen Chan
Discord @AC_


# License
Unlicensed


These are my video links on JSAssessment, the video is broken because I type slowly and my dog chewed my headset so there is no audio. I tried to fix the headset and I thought the mic was working but still not. So I muted it while recording the screen.
https://www.loom.com/share/51e1295b426845a28f874a033a8f293f
https://www.loom.com/share/6bc9a0b4c34a4b05a2cc5652ddba8a7b
https://www.loom.com/share/dc07b751f6c248ad8d63fcc3144ec536
https://www.loom.com/share/0ff363cf8e604506a5c0049614cf0959
