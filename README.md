# SmartQueue: Hypixel review build

This branch is for Hypixel staff reviewing SmartQueue's API application. It
holds no source code; the app is available as a download.

**[Download the review build (v1.5.0)](../../releases/tag/v1.5.0-review)**

> **Not affiliated with or endorsed by Hypixel.**

## How to try it
1. Run **SmartQueue-Setup-1.5.0.exe**, or unzip the portable version and run
   `SmartQueue.exe`. Windows may say "Windows protected your PC" because the
   app isn't code-signed yet: click **More info -> Run anyway**.
2. Sign in with Discord in your browser. SmartQueue never sees your password.
3. Link your Minecraft account. It links when its Hypixel profile (My Profile
   -> Social Media -> Discord) shows the same Discord account.
4. Start Minecraft and join Bedwars. Players in your lobby appear in the Lobby
   tab, and typing `/who` lists everyone in the game.

This is a pre-release. Player lookups in it run on a temporary developer key
while the application is under review.

## What it does
- **Lobby**: detects the players in your game and shows their Bedwars stats
  (stars, FKDR, WLR, finals, wins) with a threat level, most dangerous first.
  Flags likely smurfs and nicked players.
- **Compact mode**: after `/who` in a game, a slim bar along the top of the
  screen shows the top 5 threats in the lobby. It's off by default and toggled
  with a button or hotkey.
- **Teammates**: for Bedwars Lobby 1. Set the stats you want in a teammate;
  anyone who mentions your name, messages you or invites you to a party is
  checked against them.
- **Player tags and notes**: your own tags and notes on players, plus how many
  games you've played with them. Stored only on your PC.
- **My Stats and Goals**: your own progress and goals, counted from your own
  Minecraft logs.
- **Radar**: the sweatiest and least sweaty maps of the last 7 days, based on
  how many strong players SmartQueue users met per game on each map. Only map,
  mode and counts are shared, never player names.

## How it works
- SmartQueue is a **separate program, not a Minecraft mod**. It reads the chat
  log your own Minecraft client writes (`latest.log`) to see who is in your
  lobby.
- It **never modifies the game, never sends chat or commands, never automates
  anything**, and doesn't read game memory. It doesn't try to reveal who a
  nicked player really is.
- The API key is kept on SmartQueue's server, never in the app, and users never
  need their own key.
- Lookups are made only for players in your lobby, players who contact you in
  the teammate finder, manual lookups, and your own stats when you open My
  Stats or Goals. There is no polling or session tracking.
- Other players' results are cached on the server for 6 hours and shared
  between users. Your own stats are cached for 10 minutes. Each user is rate
  limited.

---
SmartQueue is an independent project. "Hypixel" and "Bedwars" belong to
Hypixel Inc.; "Minecraft" belongs to Mojang AB. This project is not affiliated
with either.
