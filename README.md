# Finn and Bones Mod by Zuzu

---

This is a complete, modded copy of Finn and Bones (Adventure Time), built on top of
the original game via FFDec decompile/recompile.

Folders:
- game/      The full playable game. Run main.swf with Ruffle (included) or a Flash
             projector. This is the only folder you need to play.
- mod_src/   The modified ActionScript 3 source files used to recompile main.swf.
             Kept for reference / future edits, not needed to play.
- Ruffle/    A standalone copy of the Ruffle Flash emulator, included so this package
             runs on its own without needing to install anything separately.

## How to run the game

1. Open the Ruffle/ folder and run ruffle.exe.
2. In Ruffle, use File > Open File (or drag-and-drop) and pick game/main.swf.
3. The game should boot straight into the main menu. If the screen stays black and
   nothing loads, close Ruffle completely and repeat steps 1-2. This sometimes
   happens on the very first load and reopening fixes it every time.

## Main features added

- Fixed buttons that broke due to animation-timing bugs (the recipe book's next-page
  arrow could become unclickable), plus a couple of other original bugs: a tip
  popup that froze the player, and a leftover mixer "hourglass" graphic that didn't
  disappear.
- Legendary Ice & Fire Dungeons unlocked (were permanently locked since 2013).
- Items that existed in the game's files but were never actually used in-game have
  been added back in: Terry's Cap (built from unused art), Boss Pendant, and Snail
  Shell now have real in-game drop locations (Stage 8, Stage 30 and Stage 4
  respectively).
- Inventory item stacking (99 cap) with Minecraft-style controls: Shift+Click sends
  an item to/from the mixer or your gear, Alt+Click collects all matching items into
  one slot, Ctrl+Click splits a stack in half.
- Enter starts the Mix.
- R opens the recipe book.
- K opens a menu with QOL/hotkey info, and also lets you set a custom player name
  that's shown above Finn's HP bar in battle.

> [!WARNING]
> **IMPORTANT: do not alternate between game/main.swf and game/main_original_backup.swf
> on the same save file.**

Ruffle (and Flash) save your progress to a single shared local-storage slot keyed to
this game, not to the SWF file you happen to run - so both versions read and write
the exact same save data. The modded game stores extra information the original game
does not understand, most importantly a "quantity" field on every item so stacks of
more than one can exist. The original main_original_backup.swf has no concept of
stacking at all: if you load a save made by the modded game, every stacked slot
silently collapses down to just 1 of that item, and the rest of the stack is gone
for good - this is not a crash, the game loads fine, the items are just quietly
dropped. Progress made in the previously-locked Legendary Ice/Fire Dungeons can also
appear locked again if viewed from the original build, since that unlock doesn't
exist in the original code.
main_original_backup.swf is kept purely as a safety net for the SWF file itself (in
case you ever want to abandon the mod entirely and start clean) - it is not meant to
be played interchangeably with game/main.swf on the same save.

Backup made: 2026-10-25.

## Download

<div align="center">

<a href="Finn%20and%20Bones%20mod%20by%20Zuzu.zip"><strong>Download Finn and Bones Mod by Zuzu</strong></a>

</div>
