# Taskbot: Open Source Discord Bot

This repository contains an open-source Discord bot built with Discord.js and MongoDB. The bot is designed to manage tasks on different boards within a guild. Below are the instructions to run the bot locally on your machine.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (v16.11.0 or higher)
- [MongoDB](https://www.mongodb.com/) (Make sure the MongoDB server is running)

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/haith2m/taskbot.git
	```

2. Navigate to the project directory:

	```bash
	cd taskbot
	```

3. Install dependencies using npm:

	```bash
	npm install
	```

4. Create a .env file in the root directory and add the following environment variables:

	```bash
	DISCORD_BOT_TOKEN=YOUR_DISCORD_BOT_TOKEN
	MONGO_URI=YOUR_MONGO_DB_CONNECTION_STRING
	GUILD_ID=YOUR_DISCORD_GUILD_ID
	CLIENT_ID=YOUR_DISCORD_CLIENT_ID
	```
Replace **YOUR_DISCORD_BOT_TOKEN**, **YOUR_MONGO_DB_CONNECTION_STRING**, **YOUR_DISCORD_GUILD_ID**, and **YOUR_DISCORD_CLIENT_ID** with your own values.

## Database Setup

1. Ensure your MongoDB server is running.

2. The bot uses a MongoDB database to store board and task information. Make sure to configure your MongoDB connection string in the .env file as MONGO_URI.


## Registering Bot Commands

1. Run the registerCommands.js script to register slash commands with Discord API:

	```bash
	node registerCommands.js
	```

This script reads commands from the **`commands`** directory and registers them with the specified guild.

## Running the Bot

1. Start the bot by running the following command:

	```bash
	node index.js
	```

The bot will log its status once it's successfully connected to Discord and MongoDB.

## Bot Usage
Use `/help` to view all commands in the bot.

Use `/command-name` to interact with the bot. Replace command-name with the name of the command you want to use.

## Contributing
Feel free to contribute to this open-source project by creating issues, suggesting improvements, or submitting pull requests.