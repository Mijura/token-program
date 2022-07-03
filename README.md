# Token Program
Solana Blockchain Developer Bootcamp Token Program

## Setup instrcutions

1) Install Node.js

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
nvm install node
```

Check node and npm version:

```bash
node -v
npm -v
```

2) Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

After executing command, follow instructions to install Rust. At the end check the version by executing following command:

```bash
rustc --version
```

3) Install Solana Tool Suite for compailing and deploying smart contracts

```bash
sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
```

Verify installation with by executing command:

```bash
solana --version
```

4) Tesing your setup

Generate keypair account and get some SOL tokens:

```bash
solana-keygen new
solana airdrop 2
```

## Run instructions

1) Run local validator

```bash

solana config set --url localhost
solana-test-validator
```

2) Compile smart contracts by positioning terminal into project folder and executing following command:

```bash
cargo build-bpf --manifest-path=./Cargo.toml --bpf-out-dir=dist/program
```

3) Deploy program:

```bash
solana program deploy dist/program/token_program.so
```

4) Run client

```bash
npm install
npm run start
```
