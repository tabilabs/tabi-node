# Tabi Node 
This repository releases the GUI installation package (Windows, Mac platform) and Linux cli program required for pre-mining.
# Getting Started
Dear Captain Node Owner, it's time to activate your Captain Node and start pre-mining on Tabi Testnet V2 Yoake. This will help you get familiar with the node usage process after the mainnet launches more quickly. We will also incentivize all captain node owners who participate in pre-mining on Tabi Testnet V2 Yoake.
## Windows GUI Installation Package
Download the latest version of the installation package `Tabi-Client-Windows-{version}-Setup.exe` 

Click to download the current version:
[Tabi-Client-Windows-0.0.1-beta-Setup.exe](https://github.com/tabilabs/tabi-node/releases/download/v0.0.1-beta/Tabi-Client-Windows-0.0.1-beta-Setup.exe)
## Mac OS GUI Installation Package
Download the latest version of the installation package `Tabi-Client-Mac-{version}-Installer.dmg`

Click to download the current version:
[Tabi-Client-Mac-0.0.1-beta-Installer.dmg](https://github.com/tabilabs/tabi-node/releases/download/v0.0.1-beta/Tabi-Client-Mac-0.0.1-beta-Installer.dmg)

## CLI Program
### Download
####  Linux Amd64( X86_64)
`
wget https://github.com/tabilabs/tabi-node/releases/download/v0.0.1-beta/node-cli-amd64-linux-0.0.1-beta.tar.gz
`
####  Linux Arm64
`
wget https://github.com/tabilabs/tabi-node/releases/download/v0.0.1-beta/node-cli-arm-linux-0.0.1-beta.tar.gz
`
####  Macos Amd64( X86_64): Intel series processor chips(eg: i7, i5, i3)

Click to download the current version:
[node-cli-amd64-mac-0.0.1-beta.tar.gz](https://github.com/tabilabs/tabi-node/releases/download/v0.0.1-beta/node-cli-amd64-mac-0.0.1-beta.tar.gz)

####  Macos Arm64: Apple series processor chips(eg: M1, M2, M3)

Click to download the current version:
[node-cli-arm-mac-0.0.1-beta.tar.gz](https://github.com/tabilabs/tabi-node/releases/download/v0.0.1-beta/node-cli-arm-mac-0.0.1-beta.tar.gz)

### Install
After successful download, you can install it with the following command:

`
sudo tar -zxvf ./node-cli-arm-linux-0.0.1-beta.tar.gz -C /usr/local/bin/
`

Tips: Please replace the `node-cli-arm-linux-0.0.1-beta.tar.gz` name with the name of the software package you downloaded.

After the command is executed, you can enter the following command to verify whether the installation is successful
node-cli version.

If the exec format error: node-cli error appears, it means that the system architecture (Amd64/Arm) does not match the file.


# Run Node 

## Windows And Mac GUI Operation Guide
You can run the tabi node by following the [Graphic Tutorial](https://blog.tabi.lol/#/article/36)

## CLI Program Operation Guide

### 1. Wallet Command
You can use the following command to view wallet related instructions

` 
node-cli wallet
`
#### Import wallet address
If you already have a wallet address, use the following command to import the wallet: (Please delete the leading 0x from the wallet private key)

`
node-cli wallet import {private_key}
`

#### Create new wallet
You can create a new wallet using the following command:

`
node-cli wallet create
`

After the command is successfully executed, you will see your wallet mnemonic, please save it safely. We will not be able to recover your wallet if it is lost.

#### Export current wallet
You can use the following command to export the private key of the current wallet:

`
node-cli wallet export
`

#### View the current wallet address
You can use the following command to view the current wallet address:

`
node-cli wallet show
`
#### Delete the current wallet address
If you want to change a wallet address, you can use the following command to delete the current wallet address:

`
node-cli wallet delete
`

### 2. Nodes Command
#### Query all nodes of the current wallet address
How to get nodes? Click here [https://app.tabichain.com/](https://app.tabichain.com/)

`
node-cli nodes list
`

#### Approve nodes
If you want to accept some nodes and mine for them, please use the following command:

`
node-cli nodes approve
`

#### Start mining
Please use the following command to mine:

`
node-cli nodes mining
`

After running the mining command, you will see some printed information, please do not end the process.

You can use nohup, screen, supervisor, etc. to maintain the process.
For example, use nohup:

`
nohup node-cli nodes mining &
`