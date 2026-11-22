[README.md](https://github.com/user-attachments/files/35229228/README.md)
# Texture Painter

A free website for painting Minecraft Java PvP item textures, pixel by pixel, with a 3D preview.
Made by krisz (with Claude) for his PvP resource pack.

Website: https://chriscodeclaude.github.io/texture-painter/

## What it does

- Covers all 58 main PvP items: weapons, armor, food, potions, movement items and explosives.
- Every item starts **full white**, already in the right shape.
- The middle shows the item in **3D**: drag to spin, scroll or pinch to zoom, tap a pixel to paint it.
- On the right, a flat pixel grid you can click or drag to paint.
- Colours: 5 theme colours, 32 more, and a colour picker for any colour.
- **↶ Undo** button (or Ctrl+Z): one press undoes one tap or one drag.
- Works on phones (one column: item list on top, then 3D view, then the grid).
- Your painting is saved in your own browser, so a reload doesn't lose it. Other people
  don't see your painting.

## Saving

| Button | What you get |
|--------|--------------|
| Download this item (.png) | the open item, with its Minecraft file name (e.g. `diamond_sword.png`) |
| Download pack (.zip) | a ready resource pack with every item you painted; put it in `.minecraft/resourcepacks` |
| Connect pack folder / Save to pack folder | computer only (Chrome/Edge): writes straight into a pack folder |

## Theme colours

| Colour | Hex |
|--------|-----|
| Dark navy | #1E3058 |
| Steel blue | #496896 |
| Grey-blue | #A4B5D3 |
| Light blue | #B0CBE6 |
| Soft pink | #FED6CE |

## Tech facts

- One file: `index.html`. It needs internet for three.js 0.160.0 (jsdelivr) and JSZip 3.10.1 (cdnjs).
- Minecraft **Java 26.3**, resource pack format **97** (`min_format` and `max_format` are 97 in `pack.mcmeta`).
- The white item shapes were made from the real 26.3 item textures (from Mojang's official
  client.jar), so every shape matches the game.
- The tool started in the private repo `roblox-blue-prince` (branch `krisz/minecraft`,
  file `tools/texture-painter.html`), and it is also a private claude.ai page. This repo is the
  public copy so people can use it without signing in.

## Known limits

- Per-type potions, the Tipped arrow and the Enchanted golden apple save to
  `textures/item/custom/...`. The game won't use those until item model files are written (a later step).
- The Shield is the 64x64 entity sheet, shown flat, so it looks odd in 3D.
- Blocks (TNT, Respawn anchor) show one face on all 6 sides.
- The "Spear" row is the Diamond spear.

## Updating the website

When the tool changes, upload the new `index.html` here again
(Add file → Upload files → Commit changes). The site updates in about a minute.
