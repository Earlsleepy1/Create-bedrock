# Create — Bedrock conversion

This branch holds a conversion of the Java **Create** mod (6.0.10, Minecraft 1.21.1, NeoForge) into a Minecraft Bedrock addon, made with **ModBridge**.

**Status: data only, in progress.** The blocks, items, textures and vanilla-type recipes are converted and importable. The machines don't work yet — the code that makes shafts spin and millstones grind is being written now (Phase 1: kinetic network + core machines). Nothing here has been tested in-game yet.

## Files

- `create-bedrock.mcaddon` — the addon. Import it into Minecraft Bedrock and activate both packs in a world.
- `CONVERSION_REPORT.md` — the full list of what converted (1,996 items) and what didn't, including every machine, code file and custom recipe that still needs a human.

## What converted

- **1,996 items:** 643 blocks, 182 items, 469 recipes, 702 textures.

## What didn't (honest list)

- Java code can't be converted automatically: the kinetics engine, contraptions, trains, Ponder, schematics and all 1,146 custom `create:*` recipes (milling, crushing, pressing, mixing, …) are listed as TODOs in the report. They need hand-written Bedrock scripts — that's the work in progress.
- A whole team hand-writing the same thing (the Vatonage port) got about 25% of the blocks working. That's the realistic ceiling, and this conversion is aiming at it.

## Credits

- **Create** itself is by **simibubi and the Creators-of-Create team** — the original mod this is converted from. Source: <https://github.com/Creators-of-Create/Create>. This fork's Java source on `mc1.21.1/dev` is theirs, untouched.
- **Vatonage's Create Bedrock addon** — the reference for how kinetics can be faked in Bedrock scripts. The scripts being written here are original work, not copies.
- **ModBridge** — the converter that produced the data packs and this report.

## License

Create is MIT licensed (see `LICENSE` at the repo root). The conversion and the new scripts follow the same license.
