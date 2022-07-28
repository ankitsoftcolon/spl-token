
# Create Own token With Solana

Guide for creating own token with Solana


## Install Dependies

 (1)  Node.js 

 (2) Install Rust
```bash
  git clone curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

 (3) Install SPL-token CLI
```bash
  cargo install spl-token-cli
```

## Set-up Solana Wallet

(1) Create Wallet
```bash
 solana-keygen new -o ./payer.json
```
    Press Enter Generating Passphrase

(2) Configure it default
```bash
solana config set --keypair ./payer.json
```

(3) set Address on Devnet
```bash
 solana config set --url https://metaplex.devnet.rpcpool.com/
```

(4) check the process by getting result :
```bash
 solana config get
```

    Output will be: 
``` 
Config File: ~/.config/solana/cli/config.yml
RPC URL: https://metaplex.devnet.rpcpool.com/
WebSocket URL: wss://metaplex.devnet.rpcpool.com/ (computed)
Keypair Path: ~/.config/solana/devnet.json
Commitment: confirmed
```


(5) Solana Address :
```bash
 solana address
```






## Create Token

(1) Create Token (token-identifier)

```bash
  spl-token create-token 
```

``` 
Output will be: 
Creating token A2niQX3aTSJvPuPijgEm2ZVgCrYrM3jdHPAdvvPqCjsP
```
(2) Create token Account Address for holding Account

```bash
  spl-token create-account <token-identifier>
```

``` 
Output will be: 
Creating account FetankoLxj5bY4coqgjbGSTbLc9aE67nrPrb9qCHt4ER
```

(3) Mint Token

```bash
  spl-token mint <token-identifier> <token-amount>
```

``` 
Output will be: 
Minting <token-amount> tokens
  Token: A2niQX3aTSJvPuPijgEm2ZVgCrYrM3jdHPAdvvPqCjsP
  Recipient: FetankoLxj5bY4coqgjbGSTbLc9aE67nrPrb9qCHt4ER
```

(3) Mint Token

```bash
  spl-token balance <token-identifier> 
```

``` 
Output will be: 
<token-amount>
```



