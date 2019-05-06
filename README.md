# Minecraft 1.14 Mods for Realms

## Installing Fabric
Close Minecraft and Launcher.

Download fabric installer at: **https://fabricmc.net/use/**

Select "**Vanilla**" and choose "**Download installer (Universal/.JAR)**"

1. After download run the jar
2. It should show you your minecraft path
3. Click Install
4. Close the fabric installer if it's still open and open the Minecraft Launcher

## Setting up the mods folder the lazy way:
After Fabric Install open the Minecraft Launcher, you should see a new profile for **Fabric 1.14** *(fabric-loader-x.x.x+build.x-1.14+build.x)*
1. Edit the profile under **Launch Options**
2. Change the profile's game directory from ending with **.minecraft** to **.minecraft_fabric** (we do this so we don't clash with forge mods in the future)
3. Save everything and launch the profile. This will create the mods folder and setup everything for you
4. Once the game loads and you see the menu, close Minecraft

## Mods:
If you followed the above instructions you will put the mods in **.minecraft_fabric\mods**.

Shortcut: Press **Win+R** and paste **%appdata%\\.minecraft_fabric\\mods** and hit enter

### Realms Compatible Mods
* Mod Menu (Verify Mods Are Installed) - https://minecraft.curseforge.com/projects/modmenu
* Light Overlay (Shows where mobs can spawn) - https://minecraft.curseforge.com/projects/light-overlay
  * Press **F7** to toggle overlay
* HWYLA (WAILA replacement) - https://minecraft.curseforge.com/projects/hwyla
  * Shows item names and mob health when you look at them.
* REI (NEI replacement) - https://minecraft.curseforge.com/projects/roughly-enough-items
  * An alternative to the in-game recipe book. Press **O** to toggle
* Apple Skin (Food saturation vis) - https://minecraft.curseforge.com/projects/appleskin
  * Shows you how good each food item is and how it will affect your character.
* Mappy (Simple HUD Map until VoxelMap releases) - https://minecraft.curseforge.com/projects/mappy
  * First 1.14 Minimap! *See Config Changes below*
* Giselbaer's Durability Viewer - https://minecraft.curseforge.com/projects/giselbaers-durability-viewer
  * Shows armor, tool and offhand durability, and empty inventory slot count in the corner. *See Config Changes below*
* Block Meter (A Tape Measure)- https://minecraft.curseforge.com/projects/block-meter
  * Hold an item like a stick, press **M** to toggle role assignment. **Right click** to set start/stop points while assigned.
* Shulker Box Tooltip (Preview without placement) - https://minecraft.curseforge.com/projects/shulkerboxtooltip
  * Hold **Shift** while hovering mouse over shulker box to preview contents

### Config Changes
After the game launches it will create configs in **.minecraft_fabric\config**.

Here are the best configs I could come up with that don't get in the way of seeing F3 coordinates or Beacon/Potion Effects:

#### Giselbaer's Durability Viewer
Modify *defaultValue* under **HUD Corner** to 1 (bottom left) in ***config\durabilityviewer.json***
```
{
  "HUD Corner": {
    "key": "HUD Corner",
    "toolTip": "Corner 0 to 3 - bottom right, bottom left, top right, top left",
    "value": 1,
    "defaultValue": 0,
    "minValue": 0,
    "maxValue": 3
  },
```

#### Giselbaer's Durability Viewer
Modify *drawPosition* to 4 (bottom right) in ***config\mappy\mappy.cfg***
