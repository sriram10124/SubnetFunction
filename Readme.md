## SubnetFunction
Writing a contract and deploying it in mysubnet network using Avalanche CLI.

# Description
This Solidity code provides implementations for two contracts: ERC20 and Vault.

- ERC20 Contract: This contract represents a basic ERC20 token with functionalities like transferring tokens, approving spending limits, and checking balances. Here's a breakdown of its components:

# State Variables

- totalSupply: Tracks the total supply of tokens.
- balanceOf: Maps addresses to their token balances.
- allowance: Maps owner addresses to spender addresses and the corresponding allowed token amounts.
- name, symbol, decimals: Metadata variables representing the token's name, symbol, and decimal precision.
- lock: A boolean variable that allows for temporarily disabling transfers.
- Transfer: Fired upon token transfer between addresses.
- Approval: Fired upon approval of spending limit between addresses.
  
# Functions
- LockTransfer: Allows toggling the transfer functionality on/off through setting the lock variable.
- transfer: Transfers tokens from the sender's address to a specified recipient.
- approve: Approves a spender to spend a certain amount of tokens on behalf of the owner.
- transferFrom: Executes a transfer of tokens from one address to another on behalf of a specified spender.
- mint: Mints new tokens and assigns them to the sender's address.
- burn: Destroys tokens from the sender's address.

# Vault Contract
This contract serves as a vault for managing deposits and withdrawals of ERC20 tokens. Here's a breakdown of its components:

# State Variables

- token: Represents the ERC20 token contract address that the vault interacts with.
- totalSupply: Tracks the total supply of shares (vault tokens).
- balanceOf: Maps addresses to their share balances in the vault.
- Constructor: Initializes the token address upon deployment.

# Functions
- mint: Internal function to mint new shares and allocate them to an address.
- burn: Internal function to burn shares from an address.
- deposit: Allows users to deposit ERC20 tokens into the vault, minting vault shares in proportion to the deposited amount.
- withdraw: Allows users to withdraw ERC20 tokens from the vault by burning their vault shares.


Overall, this code provides a basic implementation of ERC20 token and a vault mechanism for managing token deposits and withdrawals. Users can interact with the ERC20 token directly or deposit/withdraw tokens to/from the vault. Additionally, it includes a feature to lock/unlock transfers for the ERC20 token.

# Getting Started
# Executing the code
- For the process of installing and setting up Avalanche CLI please follow the given document:
    
    https://docs.avax.network/tooling/cli-guides/install-avalanche-cli

To create a unique subnet, we first run:

    avalanche subnet create mySubnet

Follow the below steps: 

- # Subnet-EVM

- # ChainId: 7177

- # Token symbol: BMW

Let all the other configurations be the same and unchanged.

To deploy the subnet, run this command:

    avalanche subnet deploy mySubnet

# Connection to Metamask:
- Note the RPC URL , ChainId (7177) , Token symbol (BMW)
- Add a new network (Subnet) manually in your metamask wallet.
- To obtain test tokens use your private key and suffcient amount tokens will be minted to your account. 

# Authors
U Sriram

usriram186@gmail.com

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
