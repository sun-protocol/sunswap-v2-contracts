# SunSwap-v2-contracts

SunSwap V2 is the one of major iterations of the SunSwap protocol, a decentralized exchange (DEX) built on Ethereum.  
It introduced several key improvements over V1, including support for TRC20/TRC20 pairs, flash swaps, and price oracles.  
The protocol enables automated liquidity provision using a constant product formula, allowing users to trade tokens directly from liquidity pools without relying on traditional order books.  

By decentralizing token exchange and liquidity management, SunSwap V2 became a foundational building block in the DeFi ecosystem, paving the way for more advanced versions such as SunSwap V3.

---

## Core Contracts

`SunswapV2Pair`, LP token & liquidity pool，provides `mint`,`burn`,`swap` methods.

`SunswapV2Factory`, Factory contract, create the pair contracts.

`Sunswapv2Router02`, Router contract, used for liquidity management and multi-hop swaps.

---

## Deployments 

| contract                   | chain | address                            |
| :------------------------- | :---- | :--------------------------------- |
| Factory                    | TRON Mainnet | TKWJdrQkqHisa1X8HUdHEfREvTzw4pMAaY |
|                            | NILE Testnet | THomLGMLhAjMecQf9FQjbZ8a1RtwsZLrGE |
| SwapRouter                 | TRON Mainnet | TNJVzGqKBWkJxJB5XYSqGAwUTV15U24pPq |
|                            | NILE Testnet | TMn1qrmYUMSTXo9babrJLzepKZoPC7M6Sy |

---

## Compile and Deployment

To get started, first create and initialize a [NodeJS 8.0+ environment](https://github.com/nodejs/node). Next, clone the repo and install the developer dependencies:

### Setup

```bash
git clone git@github.com:sun-protocol/sunswap-v2-contracts.git
cd sunswap-v2-contracts
npm install
```

### OS requirement

- Linux
- Mac OS X

### Compile

```
npm run compile
```

### Deploying to Nile TestNet

You can deploy the SunSwap v2 **Factory** and **SunswapV2Router02** contracts to the TRON Nile TestNet using the provided scripts.

First, export your private key for the Nile TestNet account (use a **test** account, never a production key):

```bash
export PRIVATE_KEY_NILE='Your private key'
```

Then run:

```bash
npm run deploy-tron
```

This will:

- Use the `PRIVATE_KEY_NILE` environment variable to sign transactions
- Deploy the factory and related contracts to Nile
- Output the deployed addresses to the console or logs

> **Security Warning**  
> Do **not** commit or share your private key. Use environment variables or secure secrets management. For production deployment, use hardened operational security processes.

---

## Development Notes

- Review the contract source files to understand the exact AMM logic, fees, and token requirements.
- When modifying contracts, always:
  - Re-run `npm run compile`
  - Add or update tests where applicable
  - Perform manual verification on a test network before mainnet deployment

---

## Community & Support

If you have questions about this project, find bugs, or would like to contribute, you can reach the team and community via:

- [Telegram](https://t.me/SunIO_Defi)
- [Twitter](https://twitter.com/defi_sunio)

Please follow official announcements from these channels for the latest information on deployments, upgrades, and security notices.
