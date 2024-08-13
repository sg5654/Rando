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

