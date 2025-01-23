# Cryptix Network Discord Stats Bot

This is a Discord bot that fetches and displays real-time statistics from the Cryptix Network. It updates the channel names in a specific category with the latest data on max supply, circulating supply, hashrate, block rewards, and halving data. Additionally, it keeps track of the member count for a specified role and includes anti-spam features and a mining calculator command.

## How It Works

The bot fetches data using the REST API provided by the Cryptix Network. It makes HTTP GET requests to specific endpoints to retrieve the latest information on max supply, circulating supply, hashrate, block rewards, and halving data. The data is then used to update the names of specified Discord voice channels, providing real-time statistics directly within the Discord server.

## Anti-Spam Measures

The bot includes anti-spam features to prevent users from spamming messages. It tracks message history for each user and issues a timeout if a user sends the same message multiple times in a short period. The bot also monitors display names and message content for flagged keywords and takes appropriate actions such as kicking or banning the user if suspicious activity is detected.

## Calculator Command

The bot includes a calculator command (`!calc`) that allows users to estimate their mining rewards based on their hashrate. Users can enter their hashrate, and the bot will calculate and display the estimated rewards per second, minute, hour, day, week, month, and year.

## Calculator example output

```
!calc 3.14
```

```
Network Hashrate: 114.64 MH/s
Daily CYTX Mined: 928800.00 CYTX
24h Emissions: 2386.47 USD
Block Reward: 10.75 CYTX
Price per CYTX: 0.0026 USD
Your Hashrate Share: 0.003%

Estimated Rewards:
- Hour: 1.06 CYTX (0.003 USD)
- Day: 25.44 CYTX (0.065 USD)
- Week: 178.09 CYTX (0.458 USD)
- Month: 774.36 CYTX (1.990 USD)
- Year: 9292.26 CYTX (23.876 USD)
```

## Prerequisites

- Python 3.8+
- A Discord bot token
- A Discord server with appropriate permissions

## Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/cryptix-project/discord-stats-bot.git
   cd discord-stats-bot
   ```

2. Install the required Python packages:

   ```sh
   pip install -r requirements.txt
   ```

3. Configure the bot:

   - Rename the `example.env` to `.env`.
   - Open `.env` file with any text editor.

   ```
   TOKEN= # Bot Token
   ```

   - Fill in your bot token next to the `=` sign in the first line.
   - Fill in the `CHANNEL_ID` with your actual IDs.

4. Run the bot:
   ```sh
   python bot.py
   ```

## Usage

Invite the bot to your Discord server and ensure it has permissions to manage channels and read messages in the specified category. The bot will automatically update the specified channels with the latest data from the Cryptix Network and the member count for the specified role. Use the `!calc <hashrate_in_kH/s>` command to estimate mining rewards based on your hashrate.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Development Fund

The devfund is a fund managed by the Cryptix community in order to fund Cryptix development. Please consider a donation to support ongoing and future projects.

```
cryptix:qrjefk2r8wp607rmyvxmgjansqcwugjazpu2kk2r7057gltxetdvk8gl9fs0w
```

## License

This project is licensed under the MIT License.
