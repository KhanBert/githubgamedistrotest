
Scientist Slaughtherhouse MOD for Half-Life
Version 1.0

http://www.planethalflife.com/ssh

Disclaimer:
-----------
By installing Scientist Slaughterhouse, you agree to the following terms and conditions:

I (the mod author) take no responsibility for any loss of data, loss of limb, loss of life,
loss of bowel control, mental illness, spontaneous human combustion, or any other negative
effect caused by this mod (I only take credit for the good stuff).

The mod may be distributed only if this file and all the other files that came with it are
included in the redistribution, unchanged, and no money is charged for the product being
distributed.


Description:
------------
SSH is a scientist killing mod for Half-Life. I originally started it when I got really
pissed about the poor turret & beam entities in HL, while making my first scikill map
called DDI.
SSH features:
	-detailed scientist death messages
	-Scoreboard that tells exactly how many scis have been killed
	-visual damage effects for fire and electric damage. Scientists also get fx for
		radiation & cold damage
	-ability to shoot off a sci's head, now with a shoot-blood-like-a-fire-hose fx.
	-ability to cut a sci in half with an energy disk
	-ability to turn a sci into a skeleton with acid
	-more bloody gibs
	-scientist/monster target identification hud
	-extra weapons & upgrades to previous ones
	-all weapons and ammo respawn
	-players respawn too
	-new & improved monsters
	-ability for a mapper to make any monster ignore player so they won't kill you
	-better turrets instead of the boring HL ones
	-various minor changes too numerous to list here


In SSH, you are an agent of a corporation called DDI (Death & Destruction Inc.). DDI
operations are being overflowed by clones of scientists of unknown origin. (USO,
Unidentified Scientific Object?) The Nephilim Alliance has ordered you to exterminate
them all. Maybe use them for something "constructive" like weapons tests and the like.

But who cares about storylines, just go SHOOT THE BASTARDS!

Version 1.0 has 20 levels full of scientific research (read: carnage). Level 21 is the
infamous DDI "Missing Feature" sign, although with a bit overscaled compared to the one in
my first DDI map. And yes, 22 not 21. There is no level 13.
Two more levels are found under the "Hazard Course" button, in the NA training facility.
This totals 22 maps, since that missing feature sign is not counted.


Installation:
-------------
First make sure you have the latest version of Half-Life installed (1.1.1.0 at the time this was written).

Extract to your Half-Life folder. Copy tfc.wad and tfc2.wad from your
"Half-Life\tfc" folder to the "Half-Life\ssh" folder. The maps use some TFC textures, but I didn't
include the wads because they would make the installation file much larger.

Drag the included shortcut to your desktop if you want.
NOTE: The shortcut will only work if you have Half-Life installed in the default folder
(C:\Sierra\Half-Life). If not, you'll have to create your own or start SSH from the custom
game menu in HL.


Starting:
---------
Start the game with the included shortcut. Alternatively you may select "Scientist Slaughterhouse"
in the Half-Life custom game menu.

Select new game to start the game.


Control changes:
----------------
The 3rd weapon function is binded to the middle mouse button (mouse3) by default. You can change
it in the controls dialog if you don't have a 3-button mouse or just want to use a different key.

In this version there are 2 extra HUD weapon selection slots, 6 and 7. The guns didn't fit in 5
slots anymore.


HLDM Maps:
----------
Starting with v1.0, you can load a Halflife deathmatch map into SSH and scatter scientist into
it to kill with your weapons. Set ssh_randomscis to a value above zero to determine how many
scientists will be spawned. You must restart the map after turning it on, but you can change
the count without restarting. Of course, you can use the feature on any map you want to add some
scientists to, not just HLDM maps.

Example: to scatter 40 scientist into a map, type
ssh_randomscis 40
into the console. Then restart the map (or load a different one).

I recommend using ssh_rndweapons 1 with this feature. This way you can get all the SSH guns, not
just the halflife originals.

Some maps are better suited to this than others. Sometimes a map contains a location where lots
of scientists end up piling in, eventually meaning there are no scientists elsewhere because the
set limit is reached. On some maps this happens all the time. If this is the case you must just
try a different map. Sometimes you can solve a pileup just by killing the scientists. New ones
may start to spawn in better areas.

And no, this does NOT mean there is multiplayer support in SSH 1.0.


Console commands:
-----------------
Monsters in the official SSH maps are set to ignore the player, so they can help you slaughter
scientists instead of fighting you. If you want to fight them, use the ssh_hazardmode console
variable. ssh_hazardmode 1 will make all monsters (even barneys & NA units) shoot you. Setting
it to 2 or 3 will increase their priority for targeting you. With 1, they will shoot you if there
are no better targets around, with 3 they almost always shoot you and ignore the others. Set it
back to 0 to turn it off. -1 will make all monsters ignore you, even ones that aren't set to do
so in the map.


If you want monsters to fight eachother more, use the ssh_chaosmode console variable. Setting
ssh_chaosmode 1 will make monster attack anything except their own kind. For example, human
grunts would shoot human assassins and vice versa. Setting it to 2 or 3 will make them attack
everyone. Set it to 0 to turn it off. Notice that this does not affect their relation to players,
you need to use ssh_hazardmode for that.


You can randomize weapon respawns, if you get bored with the weapon placement. Set
ssh_rndweapons 1 in the console to activate this. It respawns completely random weapons, you
could pick up a glock and get a gluon gun in its place.


In addition to the old "give" cheat code that allows you to create entities, there is now an
improved version, the "create" command. This will create the entity in front of you, not inside
you, so you don't need noclip mode to make monsters and weapon projectiles won't hit you
instantly. You can also set the weapons on created monsters by appending the weapon number after
the command. See end of the entity reference (ssh_ent.html) for the different weapon codes
for all the monsters (-1 will always select a random weapon for any monster with multiple
weapons). For example, to create a human grunt with an mp5 and EMP hand grenades, type:
create monster_human_grunt 131
to the console.

Do still remember that the game only precaches models and sounds that are used in the map, and
trying to create an entity that isn't precached will CRASH the game. So only create monsters
that already appear somewhere in the map, and only create weapons that can be fired by the
player or by monsters that already appear in the map. Look below for the only exception.

Also remember that some weapon projectiles require the firing entity to give them movement
information (speed, etc). These entities will just fall to the ground or float in midair
since the create command can not provide this info.


You can precache one extra entity (monster, projectile, anything). With the console variable
ssh_precache. So, to get the nepha agent loaded so you can create them, type:
ssh_precache monster_na_agent
into the console. Since the stuff is only loaded at level start, you need to restart the level
or go to a new one (or load a savegame) after changing ssh_precache.


Yes, I know you all want to know if you can make Nepha Power Waves with "create". The answer is
yes. The entity name is "powerwave". So you can type:
create powerwave
to the console to shoot one. Of course you can't assign a target so it won't be guided, though.


Additional Stuff:
-----------------
If you don't want to be called "Gordon Freeman" when you kill a scientist, change your name by
typing:
name "Whatever-name-you-want"
into the console.

If you have a fast computer, you can set r_decals/mp_decals to a higher value in the
console, to get more blood and bullet holes on walls. The default is 4096.

The gib blood trails can be turned off by setting ssh_extrablood 0 in the console if you have a slow
computer. Set it back to 1 to turn it on again.

SSH should be able to run any singleplayer HL scikill map (or non-scikill for that matter). Just install
them normally then run them from SSH console instead of basic halflife.

Level 6 has a switch before the last scene (outside area), that allows you to set the max amount of scientists
outside between 8 and 40. This is because the original design had 40 and I thought it may be a bit too much
for slower computers. It is somewhat unlikely that there would actually be 40 scis alive at a time (when you
run that scene for a while you'll know why), but that's the limit. With 8, the number stays low all the time.
Default is 8. Don't complain its too slow if you set it to 40. You have been warned.

This version comes with a spray paint version of the NA logo that you can paint the walls with. Just press 'T'
or whatever key you have selected for the spray decal.

There is now a what's new txt file included that lists what is changed in each version. However, due to the fact
that I code faster than I list, then forget what I coded, the list may be somewhat incomplete. Especially for
the first 2 versions, I didn't quite remember which version I added the stuff in.


Cheaters Always Prosper:
------------------------
I have been asked a few times about weapon entity names & map names. So, I'm putting them here from now on.

The map names are all like: ddi_aX where X is the map number, 1 to 21.
Note: there is no level 13.
The hazard course levels are na_trnX, where X is 1 or 2.

The entity names for all the new SSH weapons are:
weapon_softgun
weapon_flamethrower
weapon_fireball
weapon_repulsor
weapon_reflector
weapon_vortexlauncher
weapon_laserhandgun
weapon_teslacoil
weapon_displacer
weapon_sniper
weapon_freezethrower
weapon_sword
also the acid ammo for flamethrower is ammo_acidtank

Mapper Info:
------------
Moved to ssh_ent.html


Credits:
--------
Mod creator:
Denix Linelli		niki.ruusunko@pp.inet.fi


Extra zombie models/skins (assassin, black ops, construction worker, civilian, cleansuit, hev suit,
drill sergeant & recruit) and the skeleton model for the scientist by
Ooppee

The level 3 (carrier) skymap by 
Alex "alX" Peterson
downloaded from http://www.planethalflife.com/crinity

The APC prefab used in level 8 and the white car in level 14 by
Paveway
downloaded from http://www.nin64.com/prefabland/

The green flatbed truck prefab in level 14 by
Dave Waters
downloaded from http://prefabs.gamedesign.net/
 (simplified by me to reduce polygon count)


-----------------------------------------------------------------------------------------
Scientist Slaughterhouse, Nephilim Alliance and the NA logo are copyright 2001-2002 Niki "Denix Linelli" Ruusunko


