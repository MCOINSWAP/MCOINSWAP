# McoinSwap

A decentralized token swapping and utility platform built on multiple EVM networks including BNB Smart Chain, Polygon, Base, and PulseChain. Swap tokens instantly, send to multiple addresses, check token security, and list your token—all in one place.

## 🌐 Live Platform

- **Website**: [https://www.mcoins.xyz/](https://www.mcoins.xyz/)
- **App**: [https://mcoins.xyz/](https://mcoins.xyz/)


## 🔗 Connect & Community

- **Email**: [info@mcoins.xyz](mailto:info@mcoins.xyz)
- **Telegram**: [https://t.me/officialMcoins](https://t.me/officialMcoins)
- **Twitter/X**: [@Mcoinswap](https://twitter.com/Mcoinswap)
- **Medium**: [https://medium.com/@mcoinswap](https://medium.com/@mcoinswap)

## Technology Stack

**Blockchain**: BNB Smart Chain, Polygon, Base, PulseChain (EVM-compatible)  
**Frontend**: React 18 + TypeScript + Vite + Tailwind CSS  
**Web3 Libraries**: wagmi, viem, RainbowKit  
**UI Components**: shadcn/ui, Radix UI  
**Forms & Validation**: React Hook Form, Zod  
**Data Fetching**: TanStack React Query  
**Charts**: Recharts  
**Smart Contract Interaction**: wagmi hooks with contract ABIs  

## 🌍 Supported Networks

| Network | Chain ID | Native Asset | Explorer |
|---------|----------|--------------|----------|
| **BNB Smart Chain Mainnet** | 56 | BNB | [BSCScan](https://bscscan.com) |
| **Polygon Mainnet** | 137 | POL | [PolygonScan](https://polygonscan.com) |
| **Base Mainnet** | 8453 | ETH | [BaseScan](https://basescan.org) |
| **PulseChain Mainnet** | 369 | PLS | [PulseScan](https://scan.pulsechain.com) |

## 📋 Smart Contract Addresses

### Swap Contract (Fee-on-Transfer, Security)
| Network | Address |
|---------|---------|
| **BNB Smart Chain** | `0x42b389eDf58bc7d2206Dd0843E0d888908dE1eFa` |
| **Polygon** | `0xDBcDc7e81DA050A8B8A1CE71FCF158bBa9F60364` |
| **Base** | `0xB61ACa6D2753bc76C08B5cD680078d4b3c7Fe3Af` |
| **PulseChain** | `0x134a7c88F1769E23444F71b2DF32519402ab5EA0` |

### Multisender Contract (Batch Transfers)
| Network | Address |
|---------|---------|
| **BNB Smart Chain** | `0x0709dE7f556F7dA462fbE5e1Dd26a31eEAfd6191` |
| **Polygon** | `0x57865ED83Ed35C01DBe4B961a79c1cB3F71D864B` |
| **Base** | `0x15E5EC313C020A63493bd19CAA27CcE8d51a50A7` |
| **PulseChain** | `0x417907662fF39094F7C10B43E1fbd58cE43C07De` |

## ✨ Key Features

### 1. **Low-Cost Token Swaps**
Swap tokens instantly with competitive pricing across multiple DEX routers with slippage tolerance and real-time price impact calculation.

### 2. **Multi-Network Support**
Trade across BNB Smart Chain, Polygon, Base, and PulseChain without leaving the platform.

### 3. **Batch Multisender**
Send tokens to multiple addresses in a single transaction. Import recipient lists via CSV, set custom amounts, and broadcast efficiently.

### 4. **Token Security Checker**
Analyze token contracts for common rug pull indicators including:
- Ownership status and timelock mechanisms
- Liquidity pool depth analysis
- Trading volume and holder distribution
- Tax rates and transfer restrictions

### 5. **Free Token Listing**
List your token in 10 seconds with no fee. Display it in the McoinSwap interface and reach thousands of traders.

### 6. **Embeddable Swap Widget**
Integrate the McoinSwap interface into your website with a single iframe. Customizable colors, chains, and token pairs.

### 7. **Advanced Swap Options**
- Fee-on-transfer token handling
- Slippage protection and customization
- Real-time price charts and market data
- Transaction simulation and gas estimation


## 🚀 Getting Started

### Prerequisites
- Node.js 16+ and npm/pnpm
- A web3 wallet (MetaMask, WalletConnect, RainbowKit supported)
- Connection to one of the supported networks

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd mcoins-swap

# Install dependencies
pnpm install

# Start development server
pnpm dev

# Build for production
pnpm build
```

### Development

```bash
# Run dev server (available at http://localhost:5173)
pnpm dev

# Run linter
pnpm lint

# Run tests
pnpm test

# Preview production build
pnpm preview
```

## 🔄 How to Use Each Feature

### Token Swap
1. Connect your wallet via the "Connect" button
2. Select source token (from) and destination token (to)
3. Enter amount to swap
4. Review price impact and slippage tolerance
5. Click "Swap" and approve in your wallet
6. Transaction processes on-chain

### Multisender
1. Go to Multisender page
2. Select recipient token
3. Upload CSV with addresses and amounts, or paste manually
4. Review total amount and gas estimate
5. Click "Send" and approve transaction
6. All recipients receive tokens in one transaction

### Rug Checker
1. Navigate to Token Security Checker
2. Enter token contract address
3. Select network
4. Review security analysis report including:
   - Owner info and permissions
   - Liquidity analysis
   - Holder distribution
   - Tax rates
5. Make informed decision before trading

### List Token
1. Go to "List Token" page
2. Enter token contract address
3. Upload token logo (PNG/SVG)
4. Add token description and links
5. Submit listing (free, instant)
6. Token appears in dropdown after verification

### Embed Widget
1. Copy iframe code from Widget page
2. Paste into your website's HTML
3. Customize with available parameters:
   - `tokenA`: Default source token
   - `tokenB`: Default destination token
   - `chainId`: Default blockchain
   - `color`: Primary brand color
4. Widget inherits your site's theme

## 🔐 Security Features

- Non-custodial design: You control your private keys
- Contract interaction via industry-standard ABIs
- Slippage protection against price manipulation
- Fee-on-transfer token detection
- Real-time security analysis with multiple checks
- No API required—all data sourced on-chain

## 📊 Supported Tokens

McoinSwap supports:
- **Native assets** (BNB, POL, ETH, PLS)
- **PancakeSwap token lists** (BNB, Base, PulseChain)
- **Custom imported tokens** via address
- **New token listings** (free)

Default pairs per chain:
- **BNB**: BNB ↔ USDT
- **Polygon**: POL ↔ USDT
- **Base**: ETH ↔ USDC
- **PulseChain**: PLS ↔ USDT

## 🛠️ Core Technologies

| Category | Technology |
|----------|-----------|
| **Blockchain Communication** | viem, wagmi, RainbowKit |
| **Frontend Framework** | React 18, TypeScript |
| **Styling** | Tailwind CSS, shadcn/ui |
| **Build Tool** | Vite |
| **State Management** | React Context, TanStack Query |
| **Forms** | React Hook Form + Zod |
| **Testing** | Vitest |

## 📝 API Routes & Functions

### Swap Hook
```typescript
const { executeSwap, isLoading } = useSwap();
await executeSwap({
  tokenA,
  tokenB,
  amountIn,
  slippage,
  chainId
});
```

### Token Info
```typescript
const { tokenData } = useTokenInfo(tokenAddress, chainId);
```

### Amount Calculation
```typescript
const { amountOut } = useGetAmountsOut(tokenA, tokenB, amount, chainId);
```

## 🌐 Embeddable Widget Parameters

```html
<iframe 
  src="https://mcoins.xyz/widget"
  width="400"
  height="600"
  frameborder="0"
  allow="clipboard-read; clipboard-write"
></iframe>
```

**Query Parameters**:
- `tokenA`: Token address (optional)
- `tokenB`: Token address (optional)
- `chainId`: Chain ID (optional)
- `color`: Hex color code (optional)
- `theme`: "light" | "dark" (optional)

## 🐛 Troubleshooting

**Wallet not connecting?**
- Ensure wallet is installed and unlocked
- Try different wallet provider (MetaMask, WalletConnect)
- Check network selection matches app

**Swap failed?**
- Verify sufficient token balance
- Check gas fees are available
- Reduce slippage tolerance
- Ensure sufficient liquidity for trade

**Token not found?**
- Add custom token via address
- Check token exists on selected network
- Verify contract address format

**Multisender rejected?**
- Verify CSV format (Address, Amount per line)
- Ensure wallet has sufficient tokens
- Check total amount with gas fees

## 📖 Documentation

Full documentation available at [https://docs.mcoins.xyz/](https://docs.mcoins.xyz/)

## 📄 Legal

- **Privacy Policy**: [https://www.mcoins.xyz/privacy](https://www.mcoins.xyz/privacy)
- **Terms of Service**: [https://www.mcoins.xyz/terms](https://www.mcoins.xyz/terms)

## 👥 Support

Need help? Reach out:
- **Email**: [info@mcoins.xyz](mailto:info@mcoins.xyz)
- **Telegram**: [https://t.me/officialMcoins](https://t.me/officialMcoins)
- **Twitter**: [@Mcoinswap](https://twitter.com/Mcoinswap)

---

**Built by the McoinSwap team**

*McoinSwap is a non-custodial DeFi platform. Always do your own research before trading. Not financial advice.*
