# Salvium Wallet CLI User Guide

## 1. Introduction

Welcome to the Salvium CLI (Command Line Interface) wallet guide. This comprehensive document will walk you through every aspect of using the Salvium wallet, from installation to advanced features. Salvium is a privacy-focused cryptocurrency that builds upon the foundations of Monero, adding new features like staking, enhanced privacy, and eventually DeFi capabilities.

## 2. Installation and Setup

### System Requirements
- Operating System: Windows 10/11, macOS 10.14+, or Linux (Ubuntu 18.04+)
- RAM: 4GB minimum, 8GB recommended
- Storage: 50GB+ free space (for full node)
- Internet: Broadband connection

### Download and Install
1. Visit the download page [salvium.io/downloads/](https://salvium.io/downloads/)
2. Choose the appropriate version for your operating system
3. Download binary, unzip and save salvium-wallet-cli.exe in an appropriate folder. Do not use a system folder.

### Antivirus and Firewall settings
Many antivirus programs may flag the Salvium CLI wallet as potentially unwanted software due to its cryptocurrency mining capabilities. This is a false positive, but it can interfere with the wallet's functionality.

1. Add wallet file to Anti Virus exceptions list.
2. Allow salvium-wallet-cli through firewall.
3. For more information see this knowledge base post: [Antivirus and Firewall Settings](https://salvium.io/salvium-knowledge-base/antivirus-and-firewall-settings/)

### First Launch
You do not need to install salvium-wallet-cli.exe, simply run the application.

1. Give permission to connect to the network via any windows system pop-up.
2. Choose your language option - currently only English is fully supported.
3. Select continue to open options page.
4. Select between Simple mode (remote node) or Advanced mode (local node)
5. Choose between Mainnet, Testnet, or Stagenet

## 3. Creating a Wallet

### New Wallet
1. Start salvium-wallet-cli
2. Choose a name and location for your wallet file
3. Write down your 25-word mnemonic seed and keep it safe
4. Set a strong password for your wallet

### Restore Wallet
1. Start salvium-wallet-cli with --restore-deterministic-wallet flag
2. Enter your 25-word mnemonic seed
3. Set a restore height (if known) to speed up synchronization
4. Choose a name and location for your wallet file
5. Set a strong password for your wallet

## 4. Synchronization

### Daemon Synchronization
- Simple mode: Connects to a remote node, no blockchain download required
- Advanced mode: Downloads the full blockchain (50 GB+)

### Wallet Synchronization
After daemon sync, your wallet will scan the blockchain for your transactions. This can take some time, especially for older wallets.

## 5. Sending Salvium
1. Use the `transfer` command
2. Enter the recipient's Salvium address
3. Enter the amount to send
4. Add an optional payment ID
5. Confirm the transaction

## 6. Receiving Salvium
1. Use the `address` command to show your main address
2. Use `integrated_address` for payments requiring a payment ID
3. Use `get_accounts` to manage subaddresses
4. Use `new_account` to create additional accounts

## 7. Transaction History
The `show_transfers` command displays all incoming and outgoing transactions. You can:
- Search transactions
- Sort by date, amount, or type
- View detailed information for each transaction

## 8. Address Book
Use the Address Book to save frequently used Salvium addresses:
1. Use `address_book add` command
2. Enter the Salvium address
3. Add a description
4. Use `address_book show` to view entries

## 9. Mining
Salvium supports solo mining directly from the wallet:
1. Use the `start_mining` command
2. Set the number of threads to use
3. Use `stop_mining` to stop

Note: Solo mining with a regular computer is unlikely to find blocks. Consider joining a mining pool for more consistent rewards.

## 10. Staking
Salvium introduces staking capabilities:
1. Use the `stake` command
2. Enter the amount you wish to stake
3. Confirm the stake transaction
4. View stakes using `show_stakes`
5. Staking is not supported on some sub wallets.

## 11. Settings
Access wallet settings using various commands:
- `set` command for various settings
- `seed` to view your mnemonic seed
- `password` to change your password
- `set_log` to adjust log level
- `set_daemon` to change node settings

## 12. Security and Privacy
- Always keep your seed phrase safe and offline
- Use a strong, unique password for your wallet
- Consider using a hardware wallet for large amounts
- Use subaddresses to enhance privacy
- Run a full node if possible for maximum privacy

## 13. Troubleshooting
- Wallet not syncing: Check your internet connection and node settings
- Incorrect balance: Try rescanning the blockchain
- Transaction stuck: Wait for more confirmations or try resyncing
- The wallet automatically starts a background daemon that connects to the blockchain. It is not possible to run two daemons on the same machine. If your daemon isn't working, confirm that you are not running another daemon elsewhere. It is possible that a background daemon stops users from connecting with a CLI Daemon. If this happens, check open tasks to confirm if a daemon is running.

## 14. Glossary
- Salvium (SAL): The native cryptocurrency of the Salvium network
- Mnemonic Seed: 25-word phrase used to recover your wallet
- Subaddress: Unique addresses generated from your main address for enhanced privacy
- Stake: Locking up SAL to support network operations and earn rewards
- DeFi: Decentralized Finance features built into Salvium

Remember, this guide is a living document and will be updated as new features are added to Salvium. Always refer to the official Salvium website and documentation for the most up-to-date information.
