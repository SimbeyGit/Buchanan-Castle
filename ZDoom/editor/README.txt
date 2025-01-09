How to create maps using the Block Map Editor:

Before using the Block Map Editor, run Build.quadoo to create the "Output\Buchanan.PK3" data file.

The Block Map Editor allows you to edit maps in the style of Wolfenstein 3D.  The maps that you edit in the editor should be saved to ".MAP" files in the "BlockMaps" folder.  When you're done editing a map, use the editor's "Export" function to export the map layout to a ".WAD" file in the "Buchanan\MAPS" folder.

When editing maps, be aware of how the map types interact with each other:
1. Doors will automatically orient themselves depending on whether walls are vertically or horizontally adjacent.
2. There must be a "floor" block under a door.
3. Secret doors only move vertically or horizontally, but they are bidirectional before being moved.
4. The "OUTSIDE" texture will be converted to show Doom's sky (when exported).  There should be wall textures at both ends of the "OUTSIDE" walls because those wall textures will be needed to complete the sky box generation.
5. Sky lights should be use at least one block away from walls.
6. You can place a single (small) item in the special wall cage constructs, and make sure that wall cage constructs have exactly ONE border with a "floor" block.
7. No "floor" blocks should border against void tiles.
8. Every map must have exactly one start spot (any direction).

Some maps are designated (via MAPINFO) as having secret exits, which lead to the secret levels.  Don't forget to define secret exits in those levels.

After exporting maps to the "Buchanan\MAPS" folder, run Build.quadoo again to create a new PK3 file with the added or updated map.

The map files should be named in the "E#L#" format.  The episode number (1, 2, or 3) is first, followed by the level number.  Episodes one and two have 10 maps each, while the third episode has 11 maps.  Level 0 is the secret level for each episode.

Episode one should only contain dogs, British Home Guard, and Royal Military Police (following the same pattern as Wolfenstein 3D's first episode).  Episode two should contain those enemies plus the Commando and British Officer.  The third episode contains all enemies, but the Secret Service should only appear on the final map.

Difficulty and ambush settings may be defined by placing a guard and then holding CTRL while left clicking the guard.

To remove an item/guard from a cell, paint that cell once with the void item.  Clicking again will also void the floor.  Clicking with void selected on a cell containing a solid wall type resets the wall type back to void.

If you want to jump to a specific map for testing, you can run Buchanan.wqs (from the command line) like this:
Buchanan.wqs +map E1L9
That will teleport you directly to E1L9.
