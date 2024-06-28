# solidity-assesment-again
Token Creation Guide
This Solidity contract serves as an educational tool for learning about token creation, deployment, minting, and burning on the Ethereum blockchain.

 ## Description
This smart contract, named MyToken, is designed for creating tokens and utilizing their functionalities. These functionalities include creating tokens, minting new tokens, burning existing tokens, and checking the balance of tokens.

 ## Getting Started
    Installation
     To use MyToken, download or clone the Solidity contract file provided in this repository.

  ## Execution
   To run this contract, use Remix, an online Solidity IDE. Follow these steps to get started:

   Visit the Remix website.
   Compile the MyToken contract using Remix.
   Deploy the MyToken contract on an Ethereum-compatible blockchain.
   After deployment, an account address for the token will be created. Use this address to mint tokens by specifying the required number of tokens.
   Check the balance of tokens by inputting the account address in the balance function.
   To burn tokens, enter the account address and the number of tokens to be burnt, then execute the transaction.
   This contract allows you to mint tokens, burn tokens, and track token balances.
function mint(address _to, uint256 _amount) external {
        require(_to!=address(0), "Cannot mint to zero address.");
        balances[_to]+= _amount;
        _totalSupply += _amount;
        emit Mint(_to,_amount);
    }

    function burn(address _from, uint256 _amount) external {
        require(_from!=address(0),"Cannot burn from zero address");
        require(balances[_from] >= _amount, "Cannot burn more than balance.");
        balances[_from] -= _amount;
        _totalSupply -= _amount;
        emit Burn(_from, _amount);
    }

## Authors
  Harshit Sharma
  @harshitinfinity2064@gmail.com
  ## Liscense
   this project is liscenced under the MIT liscence.
