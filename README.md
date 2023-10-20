# Token - Solidity Beginner 

This project explains the creation of token by deploying a smart contract .

## Description

I have added two functions- mint and burn to increase or decrease the token supply in that address and total supply of tokens. You can deploy it and check the working of the functions along with checking the balance of the respective addresses. You can also check the value of the initialised token name and abbreviation.

## Getting Started

Deploy the code locally on a code editor by installing solidity compiler or run it on an online IDE - Remix IDE.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., begin.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.9;

contract MyToken {

    // public variables here
    string public tokenname="Jaidev";
    string public tokenabbrv="JDV";
    uint public totalsupply=50;
    // mapping variable here
    mapping(address => uint)public balance;
    // mint function
    function mint(address _minttoaddr, uint _tovalue)public {
      totalsupply += _tovalue;
      balance[_minttoaddr] += _tovalue;
   }
    // burn function
   function burn(address _burntoaddr, uint _tovalue)public {
      if(balance[_burntoaddr]>= _tovalue){
        totalsupply -= _tovalue;
        balance[_burntoaddr] -= _tovalue;
      }
     }
  }
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile begin.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "begin.sol" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it .
## Authors

Jaidev K [@jaidevvk12@gmail.com]

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
