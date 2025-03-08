# Aicraft Auto Daily Vote Bot

This is a Node.js script that automates the process of voting on the Aicraft platform using multiple Ethereum-based wallets. The bot fetches candidates, applies referral codes, and casts votes within a user-defined random range.

## Prerequisites

Before running the bot, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v16 or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- A list of Ethereum private keys in a `private_keys.txt` file.

# Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ganjsmoke/aicraft-vote.git
   cd aicraft-vote
   ```
   

2. Install dependencies:
  ```bash
  npm i axios web3@1.8.0 chalk@2
  ```

---

## Setup

1. Prepare Private Keys:
   - Create a file named private_keys.txt in the root directory.
   - Add your Ethereum private keys, one per line. For example:
     ```
     0xYourPrivateKey1
     0xYourPrivateKey2
     0xYourPrivateKey3
     ```

---

## Bot Features

- Multi-Wallet Support: The bot can process multiple wallets sequentially.
- Random Vote Range: The user can define a range (e.g., 1-4 votes), and the bot will randomly select a number of votes within that range for each wallet.
- Referral Code Application: Automatically applies a referral code if not already applied.
- Dynamic Candidate Fetching: Fetches and shuffles candidates for voting.
- Transaction Handling: Signs and sends transactions to vote for candidates.
- Vote Confirmation: Confirms votes with the Aicraft API.
- Random Delays: Introduces random delays between wallets and votes to mimic human behavior.
- 24-Hour Cycle: Automatically restarts the voting process every 24 hours.

---

## Usage

1. Start the Bot:
   ```bash
   node index.js
   ```
   - The bot will prompt you to enter a vote range (e.g., 1,4).

3. Monitor Progress:
   - The bot logs all actions to the console, including wallet addresses, vote counts, and transaction statuses.

4. Stop the Bot:
   - Press Ctrl + C to stop the bot.

---

## Configuration

### Private Keys
- Store your private keys in private_keys.txt, one per line.

### Vote Range
- The bot will prompt you to enter a vote range (e.g., 1,4) at the start. This range will be applied to all wallets.

---

## Disclaimer

- Use at Your Own Risk: This bot is provided as-is. Use it responsibly and ensure compliance with the Aicraft platform's terms of service.
- Private Key Security: Never share your private keys. Ensure the private_keys.txt file is securely stored and not exposed.
- Testing: Test the bot on a testnet or with a small number of wallets before full deployment.

---

## Support

For questions or issues, please open an issue on the GitHub repository: https://github.com/your-repo/aicraft-vote-bot/issues.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
