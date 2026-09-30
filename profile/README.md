# <img src="https://cdn.discordapp.com/emojis/781593582455881799.webp?animated=true" alt="Slime GIF"> DQI-haX: Decompiling, Reverse engineering, Programming

Reverse engineering, tools, and data for *Dragon Quest IX: Sentinels of the Starry Skies* on the Nintendo DS.

---

# <img src="https://cdn.discordapp.com/emojis/866763396108386304.webp" alt="Krakpot WEBP" height="35"> Projects

## Reverse engineering

<details>
<summary><strong><a href="https://github.com/DQIX/dqix-decomp">dqix-decomp</a> — Matching decompilation</strong></summary>

[![USA functions](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FDQIX%2Fdqix-decomp%2Fbadges%2Fusa%2Ffunctions.json)](https://github.com/DQIX/dqix-decomp/actions/workflows/match.yml)
[![USA bytes](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FDQIX%2Fdqix-decomp%2Fbadges%2Fusa%2Fbytes.json)](https://github.com/DQIX/dqix-decomp/actions/workflows/match.yml)
[![JPN functions](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FDQIX%2Fdqix-decomp%2Fbadges%2Fjpn%2Ffunctions.json)](https://github.com/DQIX/dqix-decomp/actions/workflows/match.yml)
[![JPN bytes](https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2FDQIX%2Fdqix-decomp%2Fbadges%2Fjpn%2Fbytes.json)](https://github.com/DQIX/dqix-decomp/actions/workflows/match.yml)

* Builds a byte-identical USA or JPN ROM from disassembly and decompiled C++, using [dsd](https://github.com/AetiasHax/ds-decomp)
* Every module is verified against the original on each build
* Generates objdiff progress reports and decomp.me contexts
* New contributors: see [CONTRIBUTING.md](https://github.com/DQIX/dqix-decomp/blob/main/CONTRIBUTING.md)

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/dqix-functions">dqix-functions</a> — Shared function names for the Japanese version</strong></summary>

* Symbol files in [resymgen](https://github.com/UsernameFodder/pmdsky-debug/blob/master/docs/resymgen.md) YAML: ARM9, field and battle overlays
* Each entry has an address, name, and description
* Imports into Ghidra ([instructions](https://github.com/DQIX/dqix-functions/issues/2))
* Includes an overlay map and a glossary of the game's RNGs

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/dqix-script-disasm">dqix-script-disasm</a> — Script disassembler and assembler</strong></summary>

* Disassembles the game's binary initialization scripts (lighting, loot tables, and more) into Lua
* Reassembles edited Lua back into the binary format
* Per-script-type contexts produce readable output such as `lighting_config{ ... }`

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/ArchiveTool">ArchiveTool</a> — GP2 archive extractor and repacker</strong></summary>

* Extracts and repacks `.gp2` archives, which hold most of the game's assets
* Compresses and decompresses individual assets
* Drag-and-drop Windows executables

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/desmume-scripts">desmume-scripts</a> — Lua scripts for DeSmuME</strong></summary>

* RNG table interfaces for JPN, USA, and EUR
* On-screen displays: chest timers, item respawns, monster spawn nodes, hitboxes, terrain collision, player coordinates
* Grotto map auto-search and map data scraping
* JPN battle scripts: encounters, critical hits, dodges, fleeing, metal slimes

</details>

## Web tools

<details>
<summary><strong><a href="https://github.com/DQIX/editor">editor</a> — Save editor · <a href="https://dqix.github.io/editor/">open</a></strong></summary>

* Runs fully client-side, installable as a PWA
* Correct-by-default editing that prevents corruption
* Labeled hex editor for anything the UI doesn't cover
* Looking for a maintainer: [open an issue](https://github.com/DQIX/editor/issues) if interested

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/Grotto-Searcher">Grotto-Searcher</a> — Grotto search tool · <a href="https://dqix.github.io/Grotto-Searcher/">open</a></strong></summary>

* Search by name, level, terrain, boss, location, monster rank, depth, and chest ranks
* Flags bugged wandering-monster floors, single-monster floors, inaccessible chests and areas, softlock maps, and 4-player Multibug floors
* Chest timer searches: quickload, PPAP, 3rd chest, and a chest timer marathon tool
* Map Method (AT) search by item drop pattern or whistle-summoned monster
* Link any map directly with `?id=RRSSSS`
* English, Japanese, and Traditional Chinese

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/BattleEmulator">BattleEmulator</a> — Solo RTA battle emulator · <a href="https://dqix.github.io/BattleEmulator/">open</a></strong></summary>

* Finds the fastest winning input sequence for solo boss fights
* Wight Knight, Morag, Ragin' Contagion, Master of Nu'un, Lleviathan, Tyrantula, Grand Lizzier, Corvus
* 14–25 million simulated turns per second native, 13–16 million in the browser
* C++ compiled to x86_64 and WebAssembly

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/auction">auction</a> — DQVC auction DLC generator · <a href="https://dqix.github.io/auction/">open</a></strong></summary>

* Builds `auction.bin` DLC with any items and quantities
* Multiple languages and themes
* Output is served by custom WFC servers

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/dq9RespawnTimer">dq9RespawnTimer</a> — Item respawn timer · <a href="https://dqix.github.io/dq9RespawnTimer/">open</a></strong></summary>

* Tracks respawn timers for field pickup points across 89 areas
* Loads current timers from a `.sav` or `.dsv` save
* Syncs to the game's shared 60-second tick
* Exports timers as JSON or CSV
* Works offline from `index.html`; Japanese UI

</details>

## Randomizers

<details>
<summary><strong><a href="https://github.com/DQIX/DQIX-RANDOMIZER">DQIX-RANDOMIZER</a> — Field encounter randomizer</strong></summary>

* Replaces each field monster with one of the game's 256 field monsters, overworld model included
* Bosses, scripted battles, stats, and drops are unchanged
* Prebuilt xdelta patch for the European ROM (`YDQP`); the Python script rolls new ones

</details>

<details>
<summary><strong><a href="https://github.com/DQIX/ArchipelagoDQIX">ArchipelagoDQIX</a> — Archipelago multiworld support · <a href="https://archipelago.gg">archipelago.gg</a></strong></summary>

* Fork of [Archipelago](https://github.com/ArchipelagoMW/Archipelago) adding a [DQIX world](https://github.com/DQIX/ArchipelagoDQIX/tree/main/worlds/dqix)
* BizHawk client, European ROM
* Goal: defeat Master of Nu'un, Greygnarl, or Corvus
* Work in progress

</details>

## Community

<details>
<summary><strong><a href="https://github.com/DQIX/Collapsus">Collapsus</a> — Discord bot for The Quester's Rest</strong></summary>

* Full in-game database: recipes, quests, monsters, and grottos
* Random character generation
* Playback of the full soundtrack
* Regional term translation and cross-version lookup
* Dataset derived from in-game structures

</details>

## Archived

<details>
<summary><strong><a href="https://github.com/DQIX/Save-Editor-Decomp">Save-Editor-Decomp</a> — Decompilation of the original Windows save editor</strong></summary>

* Raw, undocumented decompilation targeting .NET 8
* Kept for reference

</details>

---

# <img src="https://cdn.discordapp.com/emojis/811350512993435689.webp" alt="Pavo WEBP" height="35"> Join the Party

[The Quester's Rest](https://discord.gg/dqix) on Discord. Research and decomp discussion happens in the [DQI-haX thread](https://discord.com/channels/655390550698098700/1266135635014582332).
