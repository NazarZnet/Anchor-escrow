# Escrow Program

This repository contains a Solana program for creating and managing token escrow transactions. The program allows users to create offers, take offers, and cancel offers using the Anchor framework.

## Features
- **Make Offer**: Lock tokens in a vault and create an offer for exchange.
- **Take Offer**: Accept an offer and exchange tokens between the maker and taker.
- **Cancel Offer**: Cancel an existing offer and return tokens to the maker.

## Prerequisites

Before running this repository, ensure you have the following installed:

- [Rust](https://www.rust-lang.org/tools/install)
- [Solana and Anchor CLI](https://docs.solana.com/cli/install-solana-cli-tools)

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/NazarZnet/Anchor-escrow.git
   cd Anchor-escrow
   ```

2. Build the program:
   ```bash
   anchor build
   ```

3. Deploy the program to a local Solana cluster:
   ```bash
   solana-test-validator
   anchor deploy
   ```

## Running Tests

To run the tests for the escrow program:

1. Start a local Solana test validator:
   ```bash
   solana-test-validator
   ```

2. Run the tests:
   ```bash
   anchor test --skip-local-validator 
   ```

## Program Instructions

### Make Offer
Locks tokens in a vault and creates an offer for exchange.

- **Parameters**:
  - `id`: Unique identifier for the offer.
  - `token_a_offered_amount`: Amount of token A to offer.
  - `token_b_wanted_amount`: Amount of token B wanted in exchange.

### Take Offer
Accepts an offer and exchanges tokens between the maker and taker.

- **Parameters**: None

### Cancel Offer
Cancels an existing offer and returns tokens to the maker.

- **Parameters**: None

## Directory Structure

- `programs/escrow/src`: Contains the program logic.
- `tests`: Contains integration tests for the program.
- `target/idl`: Contains the IDL (Interface Definition Language) file for the program.

## License

This project is licensed under the MIT License.