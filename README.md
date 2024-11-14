# Solana Swap Program

## Overview
The Solana Swap Program is a decentralized application built on the Solana blockchain using the Anchor framework. This program allows users to securely swap between two different tokens (Token A and Token B) with specified offer and acceptance conditions. 

This project leverages the **Anchor framework** for streamlined development, **SPL Token Program** for token operations, and **Solana Web3.js** for blockchain interactions.

## Table of Contents
- [Features](#features)
- [Architecture](#architecture)

## Features
- **Token Swapping**: Users can create and accept token swap offers.
- **Offer Creation**: Allows the offer-maker to specify the token amounts they wish to swap.
- **Vault Management**: Securely manages and stores tokens in vault accounts during swaps.
- **Automated Testing**: Includes end-to-end testing for swap functionality with accounts for multiple users.

## Architecture
The core components of this project include:
- **Offer Account**: Stores information about each token swap offer, including the maker, the tokens involved, and the offered/wanted amounts.
- **Vault**: A temporary account that securely holds the offered tokens until an offer is taken.
- **Anchor Program**: Defines the core logic for creating and taking offers, interacting with accounts, and managing tokens.

### Program Accounts
- **Offer**: Stores the swap offer details, including token mints, maker, and offer amount.
- **Vault**: Associated token account that holds the tokens to be swapped.

### Primary Functions
- `make_offer`: Allows a user to create a new swap offer by transferring tokens to a vault account.
- `take_offer`: Accepts an existing offer, transferring tokens between users and completing the swap.
