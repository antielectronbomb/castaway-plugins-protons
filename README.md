## unfinished and untested reverts branch

Stuff I reverted:
1. Release Enforcer
2. Rocket Jumper picking up intel again
3. Sticky Jumper picking up intel again
4. Special Delivery set (without hat) +25 HP bonus
5. Warrior's Spirit pre-Tough Break
6. Croc-O-Style Item set bonus (survive headshots)
7. Bushwacka to release version (95% accurate)
8. Darwin's Danger Shield to release version

Stuff unique to this branch:

1. Powerjack (95% accurate, it should overheal when at full hp on kill)
2. 95% accurate Demoman swords deploy and holster speeds
3. unfinished persian persuader

## Introduction
Repository for plugins used on [castaway.tf](https://castaway.tf/)

The only entirely custom plugins here are ones credited only to random (chat-adverts, etc.). Everything else is a plugin made by someone else. The credits for said plugins can be found unmodified at the top of each plugin's .sp file.

This is not a comprehensive list of all plugins used on the server, however it does include all the most relevant ones to the player experience such as the map voting, team scrambling, and weapon revert plugins. 

## Compiling

To compile the plugins, download a recent Sourcemod stable version and merge the scripting directory into the scripting directory of this repo, then use `./compile.sh <plugin_name>` to compile each plugin. 

The reverts plugin has the following dependencies:
- [TF2Items](https://github.com/nosoop/SMExt-TF2Items)
- [TF2Attributes](https://github.com/FlaminSarge/tf2attributes)
- [TF2Utils](https://github.com/nosoop/SM-TFUtils)

No other plugins have any external dependencies, and the include files for the above dependencies are within this repo.

## Additional Credits
Some or all of these plugins have been modified in some way, sometimes in major ways. I do not claim credit for these plugins and all credit goes to their original creators.

* reverts.sp - This plugin is a heavily modified version of bakugo's [weapon revert plugin](https://github.com/bakugo/sourcemod-plugins), featuring lots of new reverts and different core plugin functionality. In order to add onto it I have occasionally taken some code from NotnHeavy's gun mettle revert plugin. It has since been deleted from github, however a copy of the code can be found unmodified in the scripting/legacy directory, and the gamedata in gamedata/legacy.
* votescramble - This is a heavily modded version of the votescramble from the [uncletopia plugin repo](https://github.com/leighmacdonald/uncletopia). Their version simply calls the game's autoscrambler, while my version reimplements the scramble logic from the ground up.
* nativevotes-* - This is sapphonie's [nativevotes-updates](https://github.com/sapphonie/sourcemod-nativevotes-updated), with some small modifications and bug fixes. Most notably, the nativevotes-mapchooser has a persistent mapcycle that remains between restarts.
