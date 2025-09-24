# NS2-RPC 🚀

Show off your Nintendo Switch & Nintendo Switch 2 playtime in Discord.

## What is NS2-RPC?

NS2-RPC is a Wails + SolidJS desktop client (Windows & macOS) that lets Discord display whatever you’re playing on the **Nintendo Switch & Switch 2**.
This fork enhances the original NS-RPC by adding full Switch 2 support, UI polish, and backend wiring for new titles.

## Why this fork exists

* Original NS-RPC only supported the original Switch.
* I rewrote large parts: added Switch 2 support, cleaned up UI, reworked the backend.
* I want a lighter, faster, maintainable foundation.

## Features

* Automatically advertise “Playing on Switch 2: \[Game]” in Discord presence
* Custom status messages
* Pin/unpin games you use often
* Simple UI to pick and switch titles
* Modular game metadata — easy to extend

## Currently supported games

* Mario Kart World
* Cyberpunk 2077: Ultimate Edition

Everything else is on the TODO list.

## Known Switch 2 exclusives (as of Sept 24, 2025)

Here are some games currently marketed or widely recognized as **Switch 2 exclusives** (or “Switch 2 only” titles) according to Nintendo Life and other sources.
Use this list as reference when wiring in future games.

* Mario Kart World
* Fast Fusion
* Nintendo Switch 2 Welcome Tour
* Survival Kids
* Donkey Kong Bananza
* Drag x Drive
* Hyrule Warriors: Age of Imprisonment
* Kirby Air Riders
* The Duskbloods
* Splatoon Raiders

*(Note: many of these are announced or planned exclusives — availability or exclusivity status may change over time.)*

## Installation & Setup

1. Download a build from the **releases page**.
2. Make sure Discord is running locally before launching NS2-RPC.
3. If on Windows 10 or earlier and things break, install **WebView2** (required by Wails).
4. Launch NS2-RPC, pick a game, optionally enter a custom status, and watch Discord update.

## How to add support for a new game (basic dev steps)

1. Add the game’s metadata (name, internal identifier, icon path) to your JSON/config.
2. Hook the RPC backend: when user selects that game, send the appropriate presence payload.
3. Add the new title to the frontend UI (game picker)
4. Test it on both OS targets (Windows/macOS)
5. Merge & release

## Contributing & support

Want to help? Open an issue or PR!
Feature requests, bugs, new-game support — bring them on.