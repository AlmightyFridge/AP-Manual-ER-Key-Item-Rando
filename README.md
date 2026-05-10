# Elden Ring Key Item Randomizer for Manual Archipelago

This implementation of Elden Ring Randomizer for Manual Archipelago randomizes the default locations that key items can be placed when using the Elden Ring Item and Enemy Randomizer by thefifthmatt.<br />
<br />
**PopTracker pack available here:** https://github.com/AlmightyFridge/ER-Key-Item-Rando-Tracker


## Requirements:
- Elden Ring (PC) on current patch
- Elden Ring Item and Enemy Randomizer by thefifthmatt - https://www.nexusmods.com/eldenring/mods/428
- Glorious Merchant Mod by tomclark - https://www.nexusmods.com/eldenring/mods/5192
- The latest stable Manual Client (.apworld) - https://github.com/ManualForArchipelago/Manual/releases
- manual_eldenringkeyitemrando_almightyfridge.apworld - found in releases


## How it works:
The Item and Enemy Randomizer handles all of the in game randomization while archipelago handles the self imposed "lock and key" gameplay of the randomizer. <br /><br />
Each area now has logical requirements in the form of level cap and weapon upgrade cap items. These were determined by taking the approximate low end of the recommended level for each area as stated on the Elden Ring wiki. This article can be found here: https://eldenring.wiki.fextralife.com/Recommended+Level+by+Location <br /><br />
You start in Limgrave with Limgrave and Weeping Peninsula unlocked (level cap 0 / stone level 0).<br /><br />
Your starting max level is 20 and your starting stone level is 0. This means you cannot level past 20 and you cannot use somber or smithing stones on your weapons, respectively. <br /><br />
Each Progressive Max Level received will increase your level cap by 10, up to a possible 150. <br /><br />
Each Progressive Stone Level will increment what somber and smithing stones you can use on your weapons. For example, with 4 Progressive Stone Levels you can use somber stone 4 on your somber weapons and smithing stone 4 on your smithing weapons. <br /><br />
Most key items have been removed as they do not lock locations in the randomizer. <br />
- Example 1: Dark Moon Ring has been removed as Moonlight Altar does not have important locations in these settings.
- Example 2: Rusty Key has been removed as Godrick the Grafted can be accessed through Gostoc opening the gate. 
<!-- -->
As the in game randomizer and the manual will have different items at each location, the Glorious Merchant Mod is used to give yourself items that the manual says you should have. This mod changes Kale's shop into a series of categorized shops where any item in the game can be found and bought for 0 runes.<br />
<br /><br />
This implementation does not try to restrict how you play, but rather where your available locations are. You will still need to pick up random items in the Lands Between to find your smithing/somber stones, your equipment, your flask upgrades, your spells, your consumables, etc.


## Setup:
Download all requirements, install the apworld, and unzip the mods in a convenient to access location.<br />
<br />
Customize your YAML file to your liking, generate and host the game as normal, then connect to your Archipelago room using the Manual Client.<br />
<br />
Open EldenRingRandomizer.exe from the Elden Ring Randomizer-[version number] folder <br />
Match the settings in the randomizer program to your chosen settings in your yaml <br />
    &emsp; Item Randomizer -> Which locations are important locations? <br />
       	&emsp;&emsp;Vanilla locations of major key items: ON <br />
        &emsp;&emsp;Major bosses: ON <br />
        &emsp;&emsp;Other bosses: OFF <br />
        &emsp;&emsp;Golden Seed trees and Sacred Tear Churches: Match your Flask Upgrade Sanity setting <br />
        &emsp;&emsp;Merchant shops: Match your Shopsanity setting <br />
    &emsp;Logic -> Game progression <br />
        &emsp;&emsp;Great Runes to access final boss: Match your Great Runes Victory setting <br />
        &emsp;&emsp;Great Runes to enter Leyndell: Match your Great Runes Capital setting <br />
        &emsp;&emsp;Great Runes to enter Mountaintops: Match your Great Runes Rold and/or Rold Medallion setting <br />
Other Important settings: <br />
    &emsp;Item Randomizer -> Major key items randomized?: To important locations <br />
    &emsp;Item Randomizer -> Item Placement -> Smithing Stone availability similar to vanilla: ON <br />
Configure the rest of the randomizer settings to your own preferences. <br />
Click "Select game exe" and find and select your eldenring.exe file (commonly found at Steam\steamapps\common\ELDEN RING\Game). <br />
Click "Add dll mod" and find and select the "ermerchant.dll" from the Glorious Merchant Mod folder you extracted previously. <br />
Make sure "reroll seed" is checked to make a new seed for the randomizer. <br />
Click "Randomize items and enemies" and wait until a green bar at the bottom of the window appears saying "Done! ..." <br />
Click "Launch Elden Ring" and start playing the game. <br />


## What do the items mean?
- Great Rune: Any Great Rune. If you lack a Great Rune in your inventory from normal gameplay, feel free to pick one from the Glorious Merchant shop. <br />
- Progressive Max Level: Starting max level is 20. Each Progressive Max Level obtained increases your level cap by 10, up to a possible level cap of 150. <br />
- Progressive Stone Level: Starting stone level is 0. Each Progressive Stone Level increases the smithing and somber smithing stone level that you can use by 1. Ancient Dragon Stones are considered to be stone level 10. <br />
- Farum Azula Stonesword Key: The location "Dragon Temple Lift Golden Seed" is the only check in this randomizer *requiring* a stonesword key through normal gameplay. If you lack a stonesword key when obtaining this item, grab one from from the Glorious Merchant shop. <br />
- Free XXXXX items: Pick one of whatever category from the Glorious Merchant menu. This can be done at your leisure. Certain talismans have upgrade versions that are meant to be +1, +2, or +3 versions of their base talisman without being named in that format; please use your judgement when selecting them. <br />
- Discard Weapon (trap): You must discard one of your actively held weapons before continuing normal play. <br />
- Fight a Minor Boss (trap): You must defeat a boss that does not send a check before you can check your next location. <br />
- Immediate Memory of Grace (trap): You must stop whatever you are doing and use the Memory of Grace item before continuing normal play. <br />


## Quirks of the implementation:
- Kale's shop is replaced with the Glorious Merchant shop. To access the Kale Shop Item check you must click "Receive Bell Bearing" in the menu when interacting with him and then give the bell bearing to the Twin    Maiden Husks in Roundtable Hold. You can then access the items he would normally sell from the Twin Maiden Husks Menu. <br />
- Generic Great Runes instead of specific Great Runes. This decision was made because the Great Runes themselves do not affect the progression of the game. As you check locations you are likely to find Great Runes in game anyway, making the use of the Glorious Merchant shop less frequent.
- Shop Checks. Marking a shop location as checked should include you buying at least one of the important items in the shop. These items include: Golden Seeds, Sacred Tears, Great Runes, Talisman Pouches, Keys, Whetstones, Miner's Bell Bearings, Key Items. As there are more locations than items, sometimes there will not be an important item in a shop. If you do not see one, mark the location as checked and move on.
- The Guidance of Grace is the "filler item" in this randomizer, but what does that mean? By default it does nothing, but ultimately it's up to you what it does. Maybe it's an extra 1 level to your level cap, maybe its a rune consumable, somber/smithing stone, or other minor item from the Glorious Merchant shop, maybe it's your cue to change something about your build, maybe it's one pushup irl, maybe you've decided thats your warp currency and you can only warp to graces if you have one. Whatever you decide, have fun with it and know that on default settings there are ~26 of them<br />

## Tips on faster runs:
In the Item and Enemy Randomizer:
- Turn on and configure the Auto-upgrade setting in the RandomizerHelper.dll in the Misc Options Tab
- Turn on all or most of the Convenience settings in Misc Options
- Turn on "Remove all weapon and spell requirements" in Misc Options
- In Enemy Randomizer -> Edit custom enemy placement..., click the "Merge all bosses" quick edit. This will give you easier bosses on average
- In Item Randomizer -> Edit custom item placement..., click on Item placements -> Core Mechanics and search for and add Remembrances to the pool. Warning: generation might fail with too many locations disabled.


## Area Level and Stone Minimum Requirements
| Area | Levels | Stones |
| ---- | ------ | ------ |
| Limgrave 	|	0 (20)| 	0 |
| Weeping Peninsula |	0 (20)| 	0 |
| Stormvale Castle		|+1 (30)|	+1 |
| Liurnia 		|+2 (40)|	+1 |
| Raya Lucaria 		|+3 (50)|	+2 |
| Ainsel River			|+3 (50)|	+2 |
| Siofra River			|+3 (50)|	+2 |
| Caelid 			|+4 (60)|	+4 |
| Altus Plateau 		|+4 (60)|	+4 |
| Nokron, Eternal City 	|+4 (60)|	+6 |
| Deeproot Depths		|+5 (70)|	+6 |
| Capital Outskirts 	|+5 (70)|	+6 |
| Mt. Gelmir 		|+5 (70)|	+6 |
| Lake of Rot 		|+5 (70)|	+6 |
| Dragonbarrow 		|+6 (80)|	+6 |
| Leyndell 		|+6 (80)|	+6 |
| Forbidden Lands 	|+7 (90)|	+8 |
| Mountaintops		|+7 (90)|	+8 |
| Consecrated Snowfield 	|+7 (90)|	+8 |
| Mohgwyn Palace 		|+8 (100)|	+8 |
| Haligtree 		|+8 (100)|	+8 |
| Farum Azula 		|+8 (100)|	+8 |
| Ashen Capital 		|+8 (100)|	+8 |
