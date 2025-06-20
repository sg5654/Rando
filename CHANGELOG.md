     .2 -   Addition of RE-824 Armour
     .1 -   Addition of all remaining warbond and superstore items. Placements still have to be updated
V3.29   -   Beginning of new Warbond implementations, P-92 Warrant
v3.28   -   Implemented a system to save your last loadout, to be reproduced upon closing the rando or refreshing
     .2 -   Greatly reduced the likelyhood of receiving the same item twice in a row. Every item will now be set to a 2% chance after each use
     .1 -   Reduced reduction penalty on boosters, there should now be more variety for top priority boosters
V3.27   -   New Warbond items, fixed button interactions on boosters not rerendering properly.
     .1 -   Added multiple boosters to be selected. This allows you to pick one in order from top to bottom depending on what your team is bringing
V3.26   -   Added a Booster randomizer, fixed up some of the styling since more space was needed
V3.25   -   Added a coordinate randomizer
     .4 -   Expensive ass DLC stuff
     .3 -   Buttons for special category
     .2 -   Fixed stuff
     .1 -   Armours related to warbond
V3.24   -   Borderline of justice Warbond items
     .5 -   Restructure of Strategems
     .4 -   Added MD-8 Gas Mines
     .3 -   Removed Explosive attribute on Seeker grenade
     .2 -   Portable Hellbomb
     .1 -   Seeker grenade
V3.23   -   Added some of the missing armour choices and started the warbond
     .4 -   Added TR-117, no idea why this was added to the game.
     .3 -   Illuminate patched in as possible faction, no further implmenetation for logic yet.
     .2 -   Added the W.A.S.P. Launcher to available strategems.
     .1 -   Added the new vehicle strategem, minor fix for directional shield missing a toggleButton
V3.22   -   Added the Killzone weapons and armour that were given to all helldivers for free. Added a piece of armour that was in the data set but didn't have an associated button due to an oversight.
            Also made some consistency changes for conventions that weren't being followed. This version also introduces some additional consistency checks that should've already existed. 
            This should now properly override data related to properties and pen stats in all scenario's.
     .1 -   Quick patch to add the StA-52 Assault Rifle
v3.21   -   Illuminate update! Adds the strategems and armour from the Urban Legends warbond, along with some slight tweaks to probabilities. The default is now a value of 50 and the max 100.
     .3 -   Changed the priority system to prioritize penetration stat over support weapons. This prevents an empty list bug and makes more sense in general.
     .2 -   Updated some tags that were included in the copy data set but not the live dataset that could cause logical inconsistancies, also updated some pen stats
     .1 -   Updated some tags that didn't feel right. Most orbitals and eagles are now no longer considered reliable explosives (for fabricators and bug holes), Sterilizer is now tagged as limited range.
v3.20   -   Added the new items from the "Truth Enforcers" Warbond
v3.19   -   Added another option to force a reliable method of blowing up fabricators and bug holes. This can be anything that is tagged as "Explosive" in my codebase. If none are found, a random grenade with
            explosive tag will be selected
v3.18   -   Revamped the "Minimum penetration for faction" (Or whatever I decide to rename it to later) option to now always check for the following condition:
            The currently selected loadout must contain at least one primary or support weapon that is not constricted by limited range or supply and has at least penetration 3. This allows more reliable damage against scout striders and gunships.
v3.17   -   Added a bunch of newly added weaponry. This includes primarily the new gas based warbond and the liberty day additions. Also contains a bug fix that prevented updates from working properly if list sizes 
            differed.
            KNOWN ISSUE: <-- Resolved The terminid armor revamp has made me wish to change the way the "min penetration for faction" works. In the future, this will be a system that checks if you have at least armor pen 3 available from either primary or support weapons.
v3.16   -   Added the new Napalm Barrage Strategem
v3.15   -   Changed the data persistence checks to a more sophisticated one. This will fix the issues in 3.14 and will allow changes in the future to be edited into the local storage without issues
v3.14   -   Added functionality for determining if an item has limited range. Now you will always be guaranteed to have an item to be able to fight gunships. 
            A new tag has been added for "Limited_Range" which will be added to any item that can't hit enemies in the air. Terminid behaviour is unchanged.
v3.13   -   Added functionality for maintaining toggle states between updates. Also fixed a bug where resetting buttons would occasionally cause a nullreference.
            KNOWN BUG: There is one issue, where toggling buttons and then attempting to reset the list won't work properly. This is beyond the scope of this project, as JavaScript is somehow changing its own code and changing the constants used for repopulating the lists. It works after refreshing.
v3.12   -   Added the Anti-Tank Mines, fixed a spelling error in "Legionnare"
v3.11   -   Added the new warbond weapons and armour. Restructured some of the internal orders to more closely represent the current structure
v3.10:  -   Added functionality for checking the current version
            Added an official Changelog file to link to within the version checking behaviour.
            I still have to make a custom jquery messagebox at some point to implement the direct clicking of a link
v3.9:   -   initial commit to git.

Already present before v3.9:

*** GTFO Rando:
- A basic randomizer for the game "GTFO" allowing a random weapon, random map and also has a random cosmetic randomizer courtesy of Twitch.tv/TheFamousPounder
- "Force new items each time" is a LEGACY UNUSED setting that forces the currently selected loadout to be missing from the selection to be picked from
- "Include x tool" Will simply remove the tool from the allowed selection of choices

- "Weighted randomisation" For any rundown, this changes the logic to not randomly select a rundown and then a mission, but rather collect every individual mission together in a list.
    Afterwards this list will be used for the random selection process. This makes it more likely to have a mission for rundowns you've unlocked more in

*** GTFO Loadout
- A very barebones UI for selecting and deselecting the desired items to be randomized. Does not currently include cosmetics. Clicking these options will toggle them on or off.

*** Maps
- A selection process for enabling missions you wish to be included in the random choices. By default all options will be enabled. Clicking these options will toggle them on or off.
    The selectiong box will dynamically change the page to show the relevant buttons to that rundown.

*** Helldivers
- An in-depth randomizer for "Helldivers II", featuring a full randomisation of weaponry, armour, faction, difficulty and strategems.
    This randomizer includes a custom made weight system that will attempt to add variety into your playstyle rather than being completely random. 
    This is primarily done in an attempt to not constantly force the same stuff and make it feel like more of a rotation system than a randomizer.
- Faction is related to the options below. You can change this to the current faction you're fighting or set it to random if you're using this to decide which faction to fight
- Force_reroll will simply remove every current selection from the possible list of choices for the next round. This should be revised at some point as it has some issues.
- Force_Support_Wep will force one of the selected strategems to be a support weapon, allowing you to control if your set is viable or not for what you're attempting to do.
- Max 1 support wep will limit the amount of support weapons to a maximum of 1, although it is still possible to not have a support weapons.
    Enabled by default
- Max 1 backpack will limit the amount of backpacks to a maximum of 1, although it is still possible to not have a backpack.
    Enabled by default
- min penetration for faction is a system that attempts to give you a fighting chance against whatever faction you're fighting against.
    This options assumes knowledge of weak points and armor penetration of different weapons and strategems. For a more in-depth guide on this, visit these two resources:
    https://invadersfromplanet.space/helldivers-2/#scope=expanded
    https://helldivers.io/Enemies
    The main enemies that are kept in mind for this are the Factory Strider for automatons (Requiring armor pen 3 on belly and backside weakpoints) and the Bile Titan (Requiring armor pen 4 on the inside of the back part of the thorax). The internal data in the randomizer has a system for penetration to be able to determine what's allowed in this list.
    Enabled by default
- lock faction is an option that will lock the faction after randomizing it the first time. If the faction has been selected instead of being on "Random" This option will have no effect
    This option is made to allow a smoother experience when going for full operations rather than individual missions
    Enabled by default
- reset lists WILL DELETE YOUR CURRENT DATA
    This is primarily a setting used for debugging, but will allow you to manually reset the list and their weighted probabilities. This generally won't be necessary as there is already an automatic update function in place that will compare your saved data to the desired data.

*** Helldiver Loadout
- A very barebones UI for selecting and deselecting the desired items to be randomized. Disabled grenade slots that cannot destroy bugholes/factories to avoid complications.
    Clicking these options will toggle them on or off.

*** Strategems
- A very barebones UI for selecting and deselecting the desired items to be randomized. Clicking these options will toggle them on or off.

