# Uniswap V3 Liquidity Manager

This repository provides a streamlined interface for interacting with the Uniswap V3 `NonfungiblePositionManager`. It simplifies the complex process of providing concentrated liquidity by handling token approvals, tick calculations, and position tracking in a single contract.

## Key Features
* **Concentrated Liquidity**: Provide liquidity within specific price ranges to maximize capital efficiency.
* **Auto-Fee Collection**: Functionality to claim earned trading fees without closing the position.
* **Slippage Control**: Implementation of `amount0Min` and `amount1Min` to protect against MEV sandwich attacks during minting.

## Usage
1. Deploy the contract with the official Uniswap V3 `NonfungiblePositionManager` address.
2. Call `mintNewPosition` with your desired token pair, fee tier, and tick ranges.
3. Use `collectAllFees` periodically to sweep earnings to your wallet.
