# Blockchain CLI Application

## Overview
This is a simple blockchain CLI application written in Rust. It allows users to create transactions, mine blocks, and adjust blockchain parameters such as difficulty and rewards.

## Features
- Create new transactions
- Mine new blocks
- Adjust mining difficulty
- Adjust mining reward
- Maintain a chain of blocks with proof-of-work and Merkle root computation

## Project Structure
```
blockchain/
│── src/
│   ├── main.rs        # Entry point of the CLI application
│   ├── blockchain.rs  # Blockchain implementation
│── Cargo.toml         # Rust package configuration
```

## Installation
Ensure you have Rust installed. If not, install it via [Rustup](https://rustup.rs/).

Clone the repository:
```sh
$ git clone https://github.com/RishinR/blockchain.git
$ cd blockchain
```

Build the project:
```sh
$ cargo build --release
```

## Usage
Run the application:
```sh
$ cargo run
```

### Menu Options
1. **New Transaction**: Adds a transaction by entering sender, receiver, and amount.
2. **Mine Block**: Mines a new block and adds it to the blockchain.
3. **Change Difficulty**: Updates the proof-of-work difficulty level.
4. **Change Reward**: Updates the mining reward for the blockchain.
5. **Exit**: Terminates the application.

## Blockchain Implementation
### `blockchain.rs`
- **Transaction**: Represents a transaction with sender, receiver, and amount.
- **Blockheader**: Stores metadata such as timestamp, nonce, previous hash, Merkle root, and difficulty.
- **Block**: Contains transactions and a block header.
- **Chain**: Manages the list of blocks, transactions, mining process, and difficulty settings.
- **Proof-of-Work**: Ensures computational work to validate a block.
- **Merkle Root Calculation**: Computes a hash-based tree structure for transaction integrity.

## Example Usage
```sh
input a miner address: miner1
Difficulty: 2
generating genesis block!
Menu
1) New Transaction
2) Mine block
3) Change Difficulty
4) Change Reward
0) Exit
Enter your choice: 1
enter sender address: Alice
enter receiver address: Bob
Enter amount: 50
transaction added
```

## Dependencies
The application uses the following Rust crates:
- `serde`, `serde_derive`: For serializing and deserializing data
- `sha2`: For SHA-256 hashing
- `chrono`: For timestamping blocks

## License
This project is open-source under the MIT License.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

