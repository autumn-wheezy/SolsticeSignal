# SolsticeSignal

Built for Base

SolsticeSignal is a compact Base-native repository that provides a straightforward “health check” for Base networks using official Coinbase tooling. It focuses on reliable, read-only RPC queries and clear explorer traceability.

## What You Get

- Base-aware network selection (Mainnet + Sepolia)
- OnchainKit wallet connection UI
- Viem reads for chainId, block height, and native balance
- Basescan references for deployments and source verification

## Networks

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

## Project Structure

app/  
- solsticeSignal.ts  
  React entry component that combines OnchainKit wallet UX with Base JSON-RPC reads.

Recommended supporting files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## How the App Works

Primary file: app/solsticeSignal.ts

Runtime flow:
- Initialize OnchainKitProvider on the selected Base chain
- Connect a wallet via OnchainKit Wallet UI
- Use Viem to query Base RPC for:
  - chainId
  - latest block number
  - native ETH balance for a provided address
- Keep explorer context available through Basescan URLs

## Libraries

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
EVM client for Base JSON-RPC reads

## Installation and Running

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run with a standard React/Vite or Next.js dev server.

## Author

GitHub: https://github.com/autumn-wheezy
Public contact (email): autumn-wheezy-0l@icloud.com 
Public contact (X): https://x.com/alinasouza_

## License

MIT License

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0xBfD67EFe08c12931e793d8E8bC6f1563aD82fC2C 

Deployment and verification:
- https://sepolia.basescan.org/address/0xBfD67EFe08c12931e793d8E8bC6f1563aD82fC2C
- https://sepolia.basescan.org/0xBfD67EFe08c12931e793d8E8bC6f1563aD82fC2C/0#code  

Contract #2 address:  
0xB0961933EdD2d24eB2F71204E359F1dfAa3f9308

Deployment and verification:
- https://sepolia.basescan.org/address/0xB0961933EdD2d24eB2F71204E359F1dfAa3f9308
- https://sepolia.basescan.org/0xB0961933EdD2d24eB2F71204E359F1dfAa3f9308/0#code  

Contract #3 address:  
0x793C42c8fdA372a71D4714aF5d7E7570FF313B16

Deployment and verification:
- https://sepolia.basescan.org/address/0x793C42c8fdA372a71D4714aF5d7E7570FF313B16 
- https://sepolia.basescan.org/0x793C42c8fdA372a71D4714aF5d7E7570FF313B16/0#code 
These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
