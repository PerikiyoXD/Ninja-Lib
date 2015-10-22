###Documentation
Information on the different assets formats used in each Phatasy Star game and how to extract them.  Tools I will be referencing are listed below. An index for how I define asset names is listed at the end of this document.

###Tools
Notable tools for extracting various assets. Will be referenced in the read me below.

|Tool name|Author|Description|
---|---|---|---
Noesis|Dick|Tool for exporting 3d models
HxD|Maël Hörz|General purpose hex editor
Puyo Tools|nickworonekin|DC/GC file export tools
VMT|Scthack|Texture Export Tools

###Phantasy Star Online ver. 2 (DC & PC)

| Asset | Exportable | Ninja-Lib | File Format |
---|---|---|---
Characters|○||.nj
Characters Animations|○|△|.pr2
Character Textures|○||.afs
Weapons|○||.nj
Set Pieces|○||.nj
Set Piece Animations|○||.nj
Enemies|○||.nj
Enemy Animations|○||.njm
Enemy Textures|○||.pvm
Stages|×||n.rel
Stage Textures|○||.pvm

###Phantasy Star Online: Blue Burst (PC)

| Asset | Exportable | Ninja-Lib | File Format |
---|---|---|---
Characters|○||.nj
Characters Animations|△||.pr2
Character Textures|○||.afs
Weapons|×||.xj
Set Pieces|×||.xj
Set Piece Animations|×||.xjm
Enemies Ep1&2|○||.nj
Enemy Animations Ep1&2|○|△|.njm2
Enemies Ep4|○||.nj
Enemy Animations Ep4|○||.njm
Enemy Textures|○||.xvm
Stages|△|△|n.rel
Stage Textures|○||.xvm

###Archive Formats

Archive formats are used consistently across each version of Phantasy Star Online. A description of each one is below.

**gsl**
**afs**
**bml**
**pvm**
**xvm**
**rel**

###File Formats

Basic Formats:
**.nj**
**.njm**
**.pvr**

Extended Formats:
**.xj**
**.njm2**
**.xjm**
**.xvr**

###Compression Formats

**prs**
**prc**


###Index
**Characters** Refers to the playable characters and classes such as Humar, or Ramar, etc. It also included NPC characters as they use the same file structure and animations.

**Weapons** Refers to any holdable weapon the character can use. Mags are also included in this category and are located in the same archive file as the player weapons.

**Set Pieces** Are objects included in environments which the player is able to interact with and is not an enemy or an NPC. These include containers, doors, switched, fences and other similar objects.

**Enemies** Are enemies outside of the lobby which the player is able to attack and defeat. Bosses are included in this category as they share the same format as other mobs.

**Stages** Refer to the maps, levels or locations in which the player, NPC's and enemies are placed in for the game to take place. This includes lobbies and areas such as the Forest or Ruins. 