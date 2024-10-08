# FuelPumpsNFT

**FuelPumpsNFT** is an advanced NFT smart contract developed for the **Fuel** blockchain. This contract supports minting, transferring, and royalty management for NFTs on Fuel.

## Features

- **Minting**: Allows users to mint unique NFTs until the maximum supply is reached.
- **Batch Minting**: Mint multiple NFTs in a single transaction.
- **Royalties**: Set and manage royalty receivers and percentages for each NFT.
- **Transfers**: NFT owners can transfer tokens to other users.
- **Ownership Tracking**: Track the NFTs owned by a particular address.
- **Supply Limit**: Enforces a maximum supply of NFTs.

## Contract Specifications

- **Chain**: Fuel blockchain
- **Maximum Supply**: 2022 NFTs
- **Royalty Cap**: Up to 100%
- **Minting**: Public minting available with supply checks

## Installation

### Prerequisites

Before running or deploying the contract, ensure the following tools are installed:

- [Git](https://git-scm.com/)
- [Fuelup](https://github.com/FuelLabs/fuelup) (Fuel's official toolchain)
- [Sway](https://fuellabs.github.io/sway/latest/introduction/installation.html) (for Fuel smart contracts)
- [Visual Studio Code](https://code.visualstudio.com/) (optional, for editing and developing the contract)

### Steps to Set Up

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/FuelPumpsNFT.git
   cd FuelPumpsNFT
   ```

2. **Install Fuel Toolchain**:
   Ensure that you have Fuel's toolchain installed via `fuelup`:
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://fuellabs.github.io/fuelup/fuelup-init.sh | sh
   ```

3. **Build the Contract**:
   Use `forc` to build the contract.
   ```bash
   forc build
   ```

4. **Run Tests**:
   To test the contract before deploying:
   ```bash
   forc test
   ```

## Usage

### Minting NFTs

You can mint NFTs by calling the `mint` function with the desired token URI (metadata link):
```bash
// Example minting command (pseudo-code):
mint("https://example.com/nft-metadata/1")
```

### Batch Minting

Batch mint NFTs by providing a list of URIs:
```bash
mint_batch(["https://example.com/nft-metadata/1", "https://example.com/nft-metadata/2"])
```

### Transfer NFTs

Transfer an NFT to another address using the `transfer` function:
```bash
transfer(token_id, recipient_address)
```

### Set Royalties

Assign royalty settings to an NFT:
```bash
set_royalties(token_id, receiver_address, percentage)
```

## Development

You can modify the smart contract in `FuelPumpsNFT.rs` or its Sway version in `src/main.sw` (if using Sway).

### Compiling & Deploying

To compile the contract:
```bash
forc build
```

To deploy the contract to the Fuel testnet:
```bash
forc deploy --url https://node-beta-1.fuel.network/graphql
```

### Contributing

Feel free to fork the project and create pull requests for new features or fixes.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
