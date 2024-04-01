DEFI-gaming
In this project, I have deployed this contract to mysubnet network using Avalanche CLI.

Description
This project contains a solidity file which is deployed to the subnet we created(steps shown in video). We can mint, burn , transfer , approve , check allowance and check balance of our tokens that we created and deployed.

Getting Started
Executing the code
In order to download the avalanche CLI and export it to your path, you can refer to the docs below to do the necessary steps.

https://docs.avax.network/tooling/cli-guides/install-avalanche-cli

In order to create a subnet, we run :

avalanche subnet create mySubnet
and choose:

Subnet-EVM

ChainId: 2567

Token symbol: SAN

Default values for the other configurations

Then to deploy, we run :

avalanche subnet deploy mySubnet
Then , in order to connect it to metamask , we note down the RPC URL, token symbol, chain ID to add network to metamask

Authors
Sangamesh Y

@sangamessshhh@gmail.com

License
This project is licensed under the MIT License - see the LICENSE.md file for details
