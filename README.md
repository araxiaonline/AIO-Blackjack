# 🎲 AIO-Blackjack - Araxia
![Lua](https://img.shields.io/badge/Lua-5.1-blue.svg)
[![Eluna](https://img.shields.io/badge/Eluna-Scripting-blue?logo=lua)](https://github.com/azerothcore/eluna)
[![AzerothCore](https://img.shields.io/badge/AzerothCore-WoW%20Server-red?logo=worldofwarcraft)](https://github.com/azerothcore/azerothcore-wotlk)
![AIO](https://img.shields.io/badge/Uses-Rochet2%20AIO-blueviolet)

---

## 📖 Overview

This project implements a custom **Blackjack game** for [AzerothCore](https://www.azerothcore.org/) using **Eluna** and **Rochet2’s AIO** framework.  
The game is hosted by an NPC named **Lord Foldemort**, and players can challenge him to Blackjack directly inside the game client.

---

## 🛠 Requirements

To run this module, you’ll need:

- [AzerothCore Server](https://www.azerothcore.org/) with [mod-eluna](https://github.com/azerothcore/mod-eluna) installed  
- [Rochet2 AIO](https://github.com/Rochet2/AIO)  

---

## 📦 Installation

### 1. Copy Files

#### Lua Scripts
Place both Lua scripts in your server’s `lua_scripts/` folder:

```
lua_scripts/BlackjackServer.lua
lua_scripts/BlackjackClient.lua
```


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
   - Copy the `BlackjackClient.lua` script into your rver's `scripts` directory (typically found in `lua_scripts` or a similar directory).
   - 
*NOTE: I Personally have both of my scripts in my `lua_scripts` folder.*


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

This project includes custom assets (card images, sounds, etc.) inside the **`MPQ/`** folder in this repository.  

#### Installation
1. Take the provided **MPQ folder** and pack it into a custom patch file (e.g. `patch-A.MPQ`).  
2. Place the MPQ into your WoW client’s `Data` directory.  
   ~~~
   World of Warcraft\Data\patch-A.MPQ
   ~~~
3. The MPQ already contains the correct directory structure:  
   ~~~
   Interface\Cards\
   Sound\Blackjack\
   ~~~
   So you don’t need to rearrange anything.

#### Notes
- You may rename the MPQ (`patch-A`, `patch-B`, etc.) but ensure it doesn’t conflict with existing patches.  
- Without this MPQ installed, card textures and sounds will not appear in-game.  




### 5. Credits

- **Custom NPC Script:** Manmadedrummer, Araxia Devs
- **Assets and Sounds:** Custom Assets made by Manmadedrummer with ChatGPT
- **Annotation in scripts by _ChatGPT (I was too lazy to write them lol)_**

## 🛠 Tech Stack

- [AzerothCore](https://www.azerothcore.org/) – Open-source MMO framework
- [Eluna](https://github.com/azerothcore/mod-eluna) – Lua engine for AzerothCore
- [AIO by Rochet2](https://github.com/Rochet2/AIO) – Client-Server communication for WoW


