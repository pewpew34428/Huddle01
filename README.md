# Huddle01 Testnet Auto Bot

## Overview
The Huddle01 Testnet Auto Bot is a powerful tool designed to automate interactions with the Huddle01 platform. It simplifies wallet management, proxy integration, and meeting participation while allowing users to earn Huddle01 points efficiently.

---

## Features
- **Wallet Management**:
  - Load existing wallets from a JSON file.
  - Generate new Ethereum wallets with custom names.
  - Save wallets securely in `wallets.json`.
  - **Support for Multiple Wallets**: Use multiple wallets simultaneously to join meetings or collect points across accounts.

- **Proxy Support**:
  - Load proxies from `proxies.txt`.
  - Supports HTTP/HTTPS and SOCKS5 proxies.
  - Handles proxy rotations and shared usage among wallets.

- **Meeting Automation**:
  - Automatically join Huddle01 meetings using Ethereum wallets.
  - Fetch geolocation, token, and peer data for seamless integration.
  - Enable audio and interact with the WebSocket server.

- **Geolocation and Server Connectivity**:
  - Fetch geolocation data for optimized server connections.
  - Connect with Huddle01 WebSocket servers for real-time communication.

- **User-Friendly CLI**:
  - Intuitive command-line interface for user interaction.
  - Options to join meetings or generate wallets.

---

## Setup Instructions

### Prerequisites
1. **Node.js**: Install [Node.js](https://nodejs.org/) (version 14 or later).
2. **npm**: Ensure `npm` is installed (comes with Node.js).
3. **Dependencies**: Install the following dependencies:
   - `axios`
   - `ethers`
   - `fs-extra`
   - `readline`
   - `uuid`
   - `https-proxy-agent`
   - `socks-proxy-agent`
   - `ws`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/pewpew34428/Huddle01.git
   cd Huddle01
   ```

2. Install dependencies:
   ```bash
   npm install axios ethers fs-extra ws readline uuid https-proxy-agent socks-proxy-agent
   ```

3. Add your files:
   - **Wallets**: Add a `wallets.json` file for pre-existing wallets (optional).
   - **Proxies**: Add a `proxies.txt` file with your proxy list (optional).

---

## Usage Guide

### Start the Bot
Run the bot using:
```bash
node huddle.js
```

### Access Key
You will be prompted to enter your access key to start the bot.

### Options
- **Join a Meeting**:
  - Enter the room ID when prompted (e.g., `abc-defg-hij`).
  - The bot will join the meeting and start collecting points.

- **Generate Wallets**:
  - Specify the number of wallets to generate.
  - Provide custom names for each wallets.

- **Use Multiple Wallets**:
  - The bot automatically loads wallets from `wallets.json`.
  - All wallets are used to join meetings in sequence or simultaneously (with proxies if provided).

---

### How to Join the Bot

- **Method 1**: (For PC/Desktop Users)
  - Refresh the web page to make the waiting room pop up.

- **Method 2**: (For Mobile Device Users)
  - To refresh the app, turn your Wi-Fi off and back on, or leave the meeting and rejoin. Go to the "Peers" section and Admit your bot.

---

## Configuration

### Files
- **wallets.json**: Stores information about Ethereum wallets.
- **proxies.txt**: Contains a list of proxies, one per line.

### Example `wallets.json` Format
```json
[
  {
    "address": "0x123...",
    "privateKey": "0xabc...",
    "mnemonic": "word1 word2...", # Your Recovery Phrase
    "name": "Wallet 1"
  },
  {
    "address": "0x456...",
    "privateKey": "0xdef...",
    "mnemonic": "word1 word2...", # Your Recovery Phrase
    "name": "Wallet 2"
  }
]
```

### Example `proxies.txt` Format
```
http://username:password@hostname:port
http://username:password@hostname:port
socks5://username:password@hostname:port
socks5://username:password@hostname:port
```

---

## Troubleshooting

### Common Issues
1. **Invalid Access Key**:
   - Ensure you’re using a valid access key.
   - Contact support if you encounter issues.

2. **Proxies Not Loading**:
   - Check if `proxies.txt` exists and contains valid proxy URLs.

3. **WebSocket Errors**:
   - Verify network connectivity.
   - Ensure the room ID is correct.

4. **Wallet Loading Issues**:
   - Ensure `wallets.json` is correctly formatted.
   - If no wallets are found, generate new ones using the bot.

---

## Support
For access key inquiries or further assistance, please contact:
- **Discord**: [@pewpew0x_34428](https://discord.com)

---

Happy botting with Huddle01!
