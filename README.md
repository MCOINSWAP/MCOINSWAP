# McoinSwap Documentation

## Table of Contents
1. [Overview](#overview)
2. [Getting Started](#getting-started)
3. [Features](#features)
4. [How to Use](#how-to-use)
5. [Supported Chains & Tokens](#supported-chains--tokens)
6. [Technical Details](#technical-details)
7. [Troubleshooting](#troubleshooting)
8. [FAQ](#faq)

---

## Overview

**McoinSwap** is a multi-chain decentralized exchange (DEX) aggregator and DeFi toolkit designed for meme coin traders and communities. It provides fast, non-custodial token swapping across multiple blockchains, plus powerful utilities like batch token transfers, rug checking, and free token listing.

### Key Highlights

- **4 Supported Chains**: BSC, Polygon, Base, and PulseChain
- **10,000+ Tokens**: Access thousands of meme coins
- **No Platform Fees**: Only pay standard DEX liquidity pool fees (0.25%)
- **Non-Custodial**: Your keys, your coins — McoinSwap never holds your funds
- **Fully Embedded**: Integrate the swap widget into your website
- **Free Token Listing**: List your token in 10 seconds

---

## Getting Started

### Prerequisites

- A Web3 wallet (MetaMask, Trust Wallet, RainbowKit, etc.)
- Native tokens for gas fees (BNB, POL, ETH, or PLS depending on chain)
- A small amount of the token you want to swap

### Connect Your Wallet

1. Visit [mcoins.xyz](https://mcoins.xyz/)
2. Click the **"Connect Wallet"** button in the top right
3. Select your wallet provider from the modal
4. Approve the connection in your wallet
5. Your wallet is now connected and you can see your balance

### Switch Chains

McoinSwap automatically detects your connected chain. To swap on a different chain:

1. Open your wallet's chain selector (e.g., in MetaMask)
2. Select one of the supported chains: **BSC**, **Polygon**, **Base**, or **PulseChain**
3. The swap interface updates automatically to show tokens on that chain

---

## Features

### 1. **Token Swaps** 🔄

Swap any token on BSC, Polygon, Base, or PulseChain with auto-optimized routing.

#### How to Swap

1. Navigate to the **Swap** page
2. **Select tokens**:
   - Click on the **"Select"** button for "You pay" to choose the token you're sending
   - Click on the **"Select"** button for "You receive" to choose the token you want to get
   - Use the **search bar** to find tokens by name, symbol, or contract address
3. **Enter amount**: Type the amount of the token you want to send
   - Use quick buttons: **25%**, **50%**, **75%**, or **Max** to quickly set amounts
4. **Review swap details**:
   - **Price rate**: 1 token = X amount of receive token
   - **Minimum received**: Guaranteed amount after slippage
   - **Price impact**: Color-coded risk indicator (green = low, yellow = moderate, red = high)
   - **Slippage tolerance**: Auto-set to 0.5% (adjustable)
5. **Confirm and execute**:
   - Click **"Swap"** button
   - Approve token spending in your wallet (first swap only)
   - Confirm the transaction
   - Wait for on-chain confirmation

#### Slippage Tolerance

Slippage is the acceptable price movement between when you submit the transaction and when it executes on-chain.

- **Auto (0.5%)**: Recommended for most liquid pairs
- **Custom**: Adjust for volatile or fee-on-transfer tokens (typical: 1–5%)

#### Fee on Transfer Tokens

Some meme coins (e.g., SHIB, QUACK) have built-in transfer taxes. If your swap fails with a fee-on-transfer token:

1. Enable the **"Fee on Transfer"** toggle at the bottom of the swap form
2. This tells the router to account for the tax
3. Try again

### 2. **Multisend** 📤

Send tokens to hundreds of wallets in a single transaction. Perfect for airdrops, community payouts, and contributor rewards.

#### How to Use Multisend

1. Navigate to the **Multisend** page
2. **Select token**: Choose which token to send
3. **Add recipients**:
   - **Paste CSV**: Paste a list of addresses and amounts (format: `address,amount`)
   - **Manual entry**: Click **"+ Add recipient"** and enter each address individually
   - **Uniform amount**: Enable to send the same amount to all addresses
4. **Review summary**:
   - Total tokens to send
   - Number of recipients
   - Estimated gas cost
5. **Confirm and execute**:
   - Click **"Send to All"**
   - Approve token spending
   - Confirm the transaction
6. **Wait for confirmation**: All transfers execute in a single batch

#### CSV Format

```
0x1234567890123456789012345678901234567890,100
0xabcdefabcdefabcdefabcdefabcdefabcdefabcd,250
0x9999999999999999999999999999999999999999,500
```

### 3. **Rug Token Checker** 🛡️

Analyze token contracts for red flags before you trade.

#### How to Check a Token

1. Navigate to the **Rug Checker** page
2. **Paste contract address**: Enter the token's smart contract address
3. **Select chain**: Choose the chain (BSC, Polygon, Base, PulseChain)
4. **Click "Check Token"**
5. **Review the report**:
   - **Honeypot risk**: Can you sell the tokens you buy?
   - **Transfer tax**: Automatic tax on buys/sells?
   - **Owner controls**: Can the owner pause trading or modify taxes?
   - **Liquidity**: Is there enough liquidity to exit?
   - **Blacklist**: Are certain wallets blocked from trading?

#### Risk Indicators

- **✅ Safe**: Low risk across all metrics
- **⚠️ Caution**: Moderate risk — review specifics
- **🚫 High Risk / Honeypot**: Do not trade

### 4. **List Your Token** 📝

Get your token listed on McoinSwap in 10 seconds — completely free.

#### How to List Your Token

1. Navigate to the **List Token** page
2. **Fill in the form**:
   - **Token Name**: Full name of your token (e.g., "MegaCoin")
   - **Symbol**: Ticker symbol (e.g., "MEGA")
   - **Contract Address**: The token's smart contract address
   - **Chain**: Select the blockchain (BSC, Polygon, Base, PulseChain)
   - **Logo URL** (optional): Direct URL to your token's logo image
   - **Website** (optional): Your project's website
   - **Description**: Brief description of your token/project
3. **Click "Submit Listing"**
4. **Confirmation**: You'll receive an email confirmation
5. **Integration**: Your token appears in the token selector within 24 hours

**Note**: Listing is free, but your token must exist on-chain and be tradeable on a supported DEX (PancakeSwap, QuickSwap, BaseSwap, PulseX).

### 5. **Embeddable Swap Widget** 💻

Embed a McoinSwap widget on your website in minutes.

#### Basic Embed

Copy this code to your website's HTML:

```html
<iframe
  src="https://mcoinswap.com/widget"
  width="480"
  height="550"
  frameborder="0"
  allow="clipboard-read; clipboard-write"
  title="McoinSwap Widget"
></iframe>
```

#### Widget Customization

You can customize the widget with URL parameters:

```html
<iframe
  src="https://mcoinswap.com/widget?tokenA=0x1234...&tokenB=0xabcd..."
  width="480"
  height="550"
  frameborder="0"
  allow="clipboard-read; clipboard-write"
  title="McoinSwap Widget"
></iframe>
```

**Parameters:**
- `tokenA`: Contract address of default "You pay" token
- `tokenB`: Contract address of default "You receive" token (locked if set)
- `chain`: Default chain ID (56 = BSC, 137 = Polygon, 8453 = Base, 369 = PulseChain)

#### Styling

The widget respects your site's light/dark theme automatically via `prefers-color-scheme`.

---

## Supported Chains & Tokens

### Supported Blockchains

| Chain | Symbol | Network | Explorer |
|-------|--------|---------|----------|
| **BNB Smart Chain** | BNB | 56 | [BscScan](https://bscscan.com) |
| **Polygon** | POL | 137 | [PolyScan](https://polygonscan.com) |
| **Base** | ETH | 8453 | [BaseScan](https://basescan.org) |
| **PulseChain** | PLS | 369 | [PulseScan](https://scan.pulsechain.com) |

### Token Support

McoinSwap supports any ERC-20 compatible token on the above chains. This includes:

- Native tokens (BNB, POL, ETH, PLS)
- Major cryptocurrencies (USDC, USDT, WETH, etc.)
- Meme coins (SHIB, DOGE, etc.)
- Custom/community tokens

**Want to add your token?** See the [List Your Token](#4-list-your-token-) section.

---

## How to Use Each Feature

### Swap Tokens

**Best for**: Trading between tokens on a single chain

**Steps**:
1. Go to `/swap`
2. Connect wallet
3. Select "You pay" and "You receive" tokens
4. Enter amount (use quick buttons or manual input)
5. Review rate and price impact
6. Adjust slippage if needed (default: 0.5%)
7. Enable "Fee on Transfer" if needed for taxed tokens
8. Click "Swap"
9. Approve spending, then confirm transaction

**Tips**:
- Start with auto slippage (0.5%)
- Increase slippage for volatile or low-liquidity pairs
- Check price impact — if > 5%, the pair may have low liquidity
- Always verify the token contract before swapping

---

### Send Tokens (Multisend)

**Best for**: Airdrops, payouts, and community distributions

**Steps**:
1. Go to `/multisend`
2. Connect wallet
3. Select the token to send
4. Add recipients:
   - Paste CSV with `address,amount` pairs, or
   - Click "+ Add" to manually add each recipient
5. Enable "Uniform Amount" if sending equal amounts to all
6. Review total tokens, recipient count, and gas estimate
7. Click "Send to All"
8. Approve spending, then confirm transaction

**CSV Example**:
```
0x111...,100
0x222...,200
0x333...,150
```

---

### Check for Rug Risk

**Best for**: Due diligence before trading a new token

**Steps**:
1. Go to `/rug-checker`
2. Paste the token contract address
3. Select the chain
4. Click "Check Token"
5. Review the analysis:
   - ✅ Honeypot safe to sell?
   - ✅ Transfer tax amount?
   - ✅ Owner capabilities?
   - ✅ Liquidity status?
   - ✅ Blacklist check?
6. **Green/✅ = Safe**, **Yellow/⚠️ = Caution**, **Red/🚫 = Avoid**

---

### List Your Token

**Best for**: Getting your token visible on McoinSwap

**Steps**:
1. Go to `/list-token`
2. Fill in all required fields:
   - Token Name, Symbol, Contract Address, Chain
3. (Optional) Add logo URL, website, description
4. Click "Submit Listing"
5. Check your email for confirmation
6. Token appears in token list within 24 hours

---

### Embed Swap Widget

**Best for**: Letting visitors swap directly from your website

**Steps**:
1. Copy the iframe code (see [Embeddable Swap Widget](#5-embeddable-swap-widget-) section)
2. Paste into your website's HTML
3. (Optional) Add `tokenA` and `tokenB` parameters to pre-select tokens
4. Save and test
5. Visitors can now swap without leaving your site

---

### Supported DEXs

McoinSwap routes through compatible DEX routers:

- **BSC**: PancakeSwap V2 Router
- **Polygon**: QuickSwap Router
- **Base**: BaseSwap / Uniswap V2 compatible
- **PulseChain**: PulseX Router

### Gas & Fees

- **McoinSwap Fee**: 0% (completely free)
- **DEX Liquidity Pool Fee**: 0.25% (built into the pool)
- **Gas Fee**: Standard network gas costs (varies by chain and congestion)

**Cost Example (BSC)**:
- Swap: ~0.002 BNB (~$0.60 at normal rates)
- Multisend (10 recipients): ~0.01 BNB (~$3.00 at normal rates)

---

## Troubleshooting

### "Wallet not connected" error

**Solution**: Click "Connect Wallet" button and approve the connection in your wallet provider.

---

### Swap transaction fails with "Slippage Exceeded"

**Cause**: Price moved too much between submission and execution (high volatility or low liquidity).

**Solutions**:
1. Increase slippage tolerance (try 1–3% for volatile pairs)
2. Try again during lower network congestion
3. Use a smaller amount
4. Check if the pair has low liquidity (price impact > 5%)

---

### "Insufficient balance" for gas

**Cause**: You don't have enough native tokens (BNB, POL, ETH, PLS) for gas fees.

**Solution**: Buy or transfer native tokens to your wallet:
- **BSC**: Get BNB from an exchange
- **Polygon**: Get POL (formerly MATIC)
- **Base**: Get ETH
- **PulseChain**: Get PLS

---

### Multisend fails with "Invalid recipient"

**Cause**: One or more addresses are malformed.

**Solutions**:
1. Check all addresses are valid 42-character hex strings (0x...)
2. Use the format: `address,amount` (one per line, no headers)
3. Remove duplicates
4. Test a small batch first

---

### Token not appearing in selector

**Cause**: Token isn't verified or listed yet.

**Solutions**:
1. **Import manually**: Click the search box and paste the contract address — hit Enter
2. **List the token**: Go to `/list-token` and submit (free, instant)
3. **Wait 24 hours**: New listings may take time to sync

---

### "Fee on Transfer" not working

**Cause**: The toggle might be off or slippage is too low.

**Solutions**:
1. Enable the "Fee on Transfer" toggle
2. Increase slippage to 2–5% (to account for the tax)
3. Verify the token has a transfer tax (check contract on block explorer)

---

### Rug Checker reports "Honeypot"

**Meaning**: The token contract prevents selling — you can't exit.

**Action**: Do not trade this token. It's a scam.

---

### Widget not loading or showing blank

**Cause**: Iframe permissions or browser blocking.

**Solutions**:
1. Verify iframe `allow` attribute includes required permissions
2. Check browser console for CSP or CORS errors
3. Ensure domain is whitelisted (contact support)
4. Clear cache and reload

---

## FAQ

### General Questions

**Q: Is McoinSwap safe?**

A: McoinSwap is non-custodial — we never hold your funds. All swaps execute directly on-chain through trusted DEX routers. Always verify token contracts on block explorers before trading.

---

**Q: Are there any fees?**

A: McoinSwap charges 0% fee. You only pay:
- DEX liquidity pool fee: 0.25% (built into every DEX)
- Network gas fees: Varies by chain and congestion

---

**Q: Which wallet should I use?**

A: Any Web3 wallet that supports the chain:
- MetaMask, Trust Wallet, WalletConnect, Coinbase Wallet, Rainbow, Ledger, etc.

---

**Q: How do I switch chains?**

A: Use your wallet's built-in chain selector. McoinSwap auto-updates when you switch.

---

### Swap Questions

**Q: What is slippage tolerance?**

A: Maximum price movement you accept between submitting and executing the transaction.
- **Auto (0.5%)**: Good for liquid pairs
- **Manual (1–5%)**: For volatile or taxed tokens

---

**Q: Why is my swap failing?**

A: Common reasons:
1. Slippage too low — increase to 1–5%
2. Insufficient gas — top up native tokens
3. Low liquidity — price impact > 5%
4. Fee-on-transfer token — enable the toggle
5. Token has blacklisted you — check contract

---

**Q: How long does a swap take?**

A: Depends on network congestion:
- **Fast**: 30 seconds – 2 minutes
- **Normal**: 2–5 minutes
- **Slow**: 5–15+ minutes (peak times)

---

**Q: Can I cancel a swap after submitting?**

A: No, once confirmed on-chain, it cannot be cancelled. Increasing gas won't help. Wait for confirmation.

---

### Multisend Questions

**Q: How many wallets can I send to at once?**

A: Theoretically unlimited, but practical limits are:
- **10–50 recipients**: Safe, typical gas ~0.01 BNB (BSC)
- **50–100**: Higher gas, be careful
- **100+**: Very high gas, consider multiple batches

---

**Q: Can I send different amounts to each wallet?**

A: Yes, use the CSV format: `address1,amount1` on each line.

---

**Q: Is there a Multisend fee?**

A: No, only gas costs.

---

### Token Listing Questions

**Q: How long until my token appears?**

A: Usually within 24 hours, but can be instant.

---

**Q: Is there a cost to list?**

A: No, listing is completely free.

---

**Q: What if my token doesn't have a logo?**

A: It's optional. Token appears with a default placeholder if not provided.

---

### Widget Questions

**Q: Can I customize the widget colors?**

A: The widget respects your site's light/dark theme via CSS. Custom theming coming soon.

---

**Q: Does the widget work on mobile?**

A: Yes, it's fully responsive.

---

**Q: Can I lock tokens in the widget?**

A: Yes, use `tokenA` and `tokenB` URL parameters to pre-select and lock tokens.

---

### Security Questions

**Q: Does McoinSwap have access to my private keys?**

A: No, absolutely not. Your wallet controls all transactions.

---

**Q: Is there a smart contract audit?**

A: McoinSwap is a frontend. Swaps execute through audited DEX routers (PancakeSwap, QuickSwap, etc.). Always verify token contracts yourself.

---

**Q: What happens if the McoinSwap website goes down?**

A: All your assets remain in your wallet. You can use other DEX frontends or contract interactions directly.

---

## Contact & Support

- **Main Website**: [https://www.mcoins.xyz/](https://www.mcoins.xyz/)
- **App URL**: [https://mcoins.xyz/](https://mcoins.xyz/)
- **Technical Docs**: [https://docs.mcoins.xyz/](https://docs.mcoins.xyz/)
- **Email Support**: [info@mcoins.xyz](mailto:info@mcoins.xyz)
- **Telegram**: [https://t.me/officialMcoins](https://t.me/officialMcoins)
- **Twitter/X**: [@Mcoinswap](https://twitter.com/Mcoinswap)
- **Medium Blog**: [https://medium.com/@mcoinswap](https://medium.com/@mcoinswap)

---

## Legal

- **Privacy Policy**: [https://www.mcoins.xyz/privacy](https://www.mcoins.xyz/privacy)
- **Terms of Service**: [https://www.mcoins.xyz/terms](https://www.mcoins.xyz/terms)

---

**Last Updated**: April 2026

**Version**: 1.0
