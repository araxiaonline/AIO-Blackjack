# AIO-Blackjack - Araxia

## Overview

This project implements a custom Blackjack game for a for AzerothCore with Eluna and it uses AIO. The game is hosted by a custom NPC, and players can interact with the NPC to play Blackjack directly in the game.

**Requires: AIO**

> **Tip**  
> **What is AIO?** AIO is a library that allows messaging from the core server and game client. This allows developers to build and deploy server-side UI changes as if they were AddOns without requiring a user to install anything. Modules in this repo that have `.client` and `.server` are AIO based modules.


## Installation

### 1. Files to Copy

#### Lua Scripts

Copy the following Lua scripts to the appropriate directories in your server:

- **Server Script:** `BlackjackServer.lua`
- **Client Script:** `BlackjackClient.lua`

#### SQL File

Copy the provided SQL file to your server's database. This file includes the necessary entries to add the Blackjack Dealer NPC to your game world.

- **SQL File:** `Blackjack-Gambler.sql`

### 2. How to Install

1. **Place the Lua Scripts:**
   - Copy the `BlackjackServer.lua` script into your server's `scripts` directory (typically found in `lua_scripts` or a similar directory).
   - Copy the `BlackjackClient.lua` script into your client's `Interface/AddOns/` directory or where your client-side scripts are stored.

2. **Run the SQL Script:**
   - Execute the `BlackjackDealer.sql` file on your WoW server database to add the Blackjack Dealer NPC to the game.

### 3. How the Game Works

1. **Interacting with the NPC:**
   - Players can approach the NPC with ID `1000000` and select one of two options: Play Blackjack or view the Rules of Blackjack.
   
2. **Playing the Game:**
   - Players pay an entry fee of 500 gold to start the game.
   - Players can place additional bets before drawing their second card, up to a maximum of 4 cards.
   - The game follows standard Blackjack rules, where the goal is to get as close to 21 as possible without going over.
   
3. **Winning and Losing:**
   - If the player wins, they receive their bet back along with an additional 500 gold.
   - If the player loses, they forfeit their bet and the game cost.

### 4. Custom Assets

Make sure any custom assets (like card images and sounds) are placed in the appropriate directories on both the client and server. For example:

- **Card Images:** Should be placed in `Interface\Cards\`

### 5. Credits

- **Custom NPC Script:** Manmadedrummer, Araxia Devs
- **Assets and Sounds:** Custom Assets made by Manmadedrumemr with ChatGPT
- **Annotation in scripts by _ChatGPT (I was too lazy to write them lol)_**

