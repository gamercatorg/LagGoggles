# LagGoggles
Intuitive lag hunting!

LagGoggles is a profiler where you can see timings in the world, visually. It comes with a custom GUI using a configurable keybind. It's compatible with [SpongeForge](https://github.com/SpongePowered/SpongeForge) and [Mixin](https://github.com/SpongePowered/Mixin), but does not require it!

##Screenshots

| LagGoggles enabled        | Normal view |
| ------------- |:-------------:|
| ![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/2-enabled.png "With laggoggles")     | ![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/2-disabled.png "Without laggoggles") |
| ![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/1-enabled.png "With laggoggles")     | ![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/1-disabled.png "Without laggoggles") |
| ![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/3-enabled.png "With laggoggles")     | ![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/3-disabled.png "Without laggoggles") |

![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/menu.png "LagGoggles menu")
![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/menu-5sec.png "LagGoggles menu")
![alt text](https://raw.githubusercontent.com/TerminatorNL/LagGoggles/master/docs/timingsmenu.png "Analyzer")

## Features
* Cross dimensional teleporting
* Sponge compatible (Not required)
* Client GUI, including overlay and clickable menus
* Colour scale for easy spotting of sources of lag.
* Calculations are done on the client, so each client can have a different colour scale.

## Configuration
* Drop the correct jar (server or client) in the /mods folder
* Serverside configuration is not required and has no effect.
* Clients can edit the config to change the colour scale.

## How it works
At startup [Mixin](https://github.com/SpongePowered/Mixin) handles each class being loaded. On the server, this mod hooks into the loading mechanism. This is the same mechanism [SpongeForge](https://github.com/SpongePowered/SpongeForge) uses, that's why it's compatible (but not required!).<br>
<br>
Entities are timed using System.nanotime() before and after the tick() and update() methods. These times are being recorded and sent to all online operators when the profiler is done.

## Benefits
* Visualisation of Tile entities and Entities.

## Dependencies
Clients work right off the bat, the server requires [Mixin](https://github.com/SpongePowered/Mixin) to work. You already have it installed if you use [SpongeForge](https://github.com/SpongePowered/SpongeForge) or [ForgeEssentials](https://github.com/ForgeEssentials/ForgeEssentials/). If you do not use either of those, simply add [Mixin](https://github.com/SpongePowered/Mixin) to the classpath.