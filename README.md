# Modified Weapon Reverts
Modified version of the Castaway Weapon Reverts Plugin for testing
Original from https://github.com/rsedxcftvgyhbujnkiqwe/castaway-plugins

Reverts I added:

Enforcer is reverted to release version:
 	
  	June 23, 2011 Patch (Über Update)
 	+20% damage done
  	0.5 sec increase in time taken to cloak
 	Random critical hits enabled.

Rocket Jumper and Sticky Jumper can pick up the intelligence again.
	
 	May 31, 2012 Patch
    	Players with the Sticky Jumper equipped cannot carry the intelligence.

Warrior's Spirit reverted to pre-Tough Break:
	
 	Pre-December 17, 2015 Patch:
	+30% damage bonus
	On Hit: Gain up to +10 health
	-20 max health on wearer
	
Special Delivery Set Bonus Restored
	
 	Pre-July 10, 2013 Patch
        +25 max health on wearer.

Croc-o-Style Set Bonus Restored
	
 	Pre-July 10, 2013 Patch
	Survive headshots with 1 HP left

Bushwacka reverted to release (Mostly, the +20% fire vulnerability only works when deployed, not on wearing. It can do random crits again.)

	June 18, 2014 Patch
    	The Bushwacka can no longer randomly Crit.
 	
  	July 2, 2015 Patch #1 (Gun Mettle Update)
    	Changed attributes:
        Changed penalty from +20% fire vulnerability to +20% damage vulnerability while active.

Darwin's Danger Shield reverted to release (flat +25 max HP buff)
	
	September 30, 2010 Patch (Mann-Conomy Update)
    	The Darwin's Danger Shield was added to the game. The attributes was:
        +25 max health on wearer.

## Readme from the original below:

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
