## Bitz Miner CLI Guide

* The first ePOW commodity token that anyone can mine on Eclipse.
* 5M max supply.
* NOT pre-mined + ZERO team/insider allocations.
* Token address: https://eclipsescan.xyz/token/64mggk2nXg6vHC1qCdsZdEFzd5QGN4id54Vbho4PswCF

## Prerequisites

* A Linux-based system (Ubuntu 20.04+ or WSL on Windows)
* A Backpack wallet (or another Eclipse-compatible wallet) 
* 0.005+ ETH on the Eclipse network

## Install Dependecies

## 1. Install Packages

```
sudo apt-get update && sudo apt-get upgrade -y

sudo apt install screen curl nano  -y
```
## 2. Install Rust

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

When Prompted, Enter 1 and wait unti installation compelete.

```
source $HOME/.cargo/env
```
## 3. Install Solana CLI:
```
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```
Close and reopen your Terminal.
```
solana --version
```
If you get solana: command not found RUN :
```
echo 'export PATH="/root/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
if using VPS, and Solana not found, REBOOT

```
reboot
```

```
solana --version
```
## 4. Switch RPC

```
solana config set --url https://bitz-000.eclipserpc.xyz/
```

##  Wallet Setup 
## Create New Keypair

```
solana-keygen new
```
 *  Press ENTER and save the passphrase.Copy your “Private Key” somewhere and then import it to Backpack Wallet. Deposit 0.005+ ETH to your wallet on Eclipse to enable mining to the wallet address you created.

Exporting PrivateKey from ID.json
```
cat ~/.config/solana/id.json
```
## Install Bitz CLI
```
cargo install bitz
```
## Run Bitz Miner

## 1. Open a screen
```
screen -S bitz
```
## 2. Start Miner
```
bitz collect
```
* The default CPU is 1. You can set the CPU cores for your Bitz miner to suit your device. For example, for 20 CPU;
first stop the node with Ctrl+C, then
enter the following command:
## Using Multiple core
```
bitz collect --cores 20
```

## Basic Commands
## Collect bitz:
 ``` 
 bitz collect
 ```
## Claim your bitz:
 ```
bitz claim
 ```
## Check your balance:
```
bitz account
```


