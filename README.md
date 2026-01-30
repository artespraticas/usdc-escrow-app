# USDC Escrow App - Arc Testnet

A decentralized escrow application for secure, time-bound USDC transactions.

## Features

- 🔒 Trustless escrow using smart contracts
- ⏱️ Time-bound transactions with auto-refund
- ✅ Mutual agreement required for fund release
- 💰 USDC stablecoin support

## Quick Start

### Prerequisites

- Node.js 18+
- MetaMask wallet
- Arc Testnet USDC (from faucet)

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/usdc-escrow-app.git
cd usdc-escrow-app

# Install dependencies
cd frontend
npm install

# Set environment variables
cp .env.example .env.local
# Edit .env.local with your contract address

# Start development server
npm run dev
```

### Environment Variables

```
VITE_CONTRACT_ADDRESS=0x8485B17B61367B1d921e8752E08eC3bd3CF3FA9B  # Your deployed contract
VITE_USDC_ADDRESS=0x3600000000000000000000000000000000000000     # USDC token on Arc Testnet
VITE_CHAIN_ID=5042002
```

## Smart Contract

The escrow contract is deployed on Arc Testnet at:
`0x...` (Add your address after deployment)

### Contract Functions

- `createEscrow(receiver, amount, duration)` - Create new escrow
- `approve(escrowId)` - Approve fund release
- `claimRefund(escrowId)` - Claim refund after timeout

## License

MIT
