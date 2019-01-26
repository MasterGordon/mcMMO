
###### **Version 2.1.0**

##### Please use Spigot or Paper!
    
    mcMMO is now built against Spigot-API instead of Bukkit

New Level Scaling

    mcMMO now features an optional 1-100 scaling mode!
    This is on by default for new installs, if you are upgrading mcMMO you will be put into Retro Mode instead (1-1000) scaling.
    The two scaling modes are the same, the changes are completely cosmetic!
    Skill Requirements in the config file will be multiplied by 10 if you are using Retro mode unless the setting has Retro in its name, keep this in mind if you need to edit anything!

World Guard Support
    
    Added support for Worldguard regions!
        "mcmmo" region flag turns on or off a players ability to use anything related to mcMMO other than commands
        "mcmmo-xp" region flag turns on or off a players ability to gain XP
        These WG flags default to on unless you specify otherwise
        
World Blacklist

    You can now disable mcMMO completely for specific worlds via world_blacklist.txt in /plugins/mcMMO/
    This file appears once mcMMO has been run at least once
    Every line of this file should be the name of a world where you don't want mcMMO to be enabled!
    
Rank System

    Skills that are not yet unlocked will show up as ??? until learned
    Many skills now make use of a rank system!
    Rank level requirements are modified in skillranks.yml
    Woodcutting's Double Drop subskill is now named Harvest Lumber
    Archery's Skill Shot now uses a rank system
    Swords' Bleed now uses a rank system
    Axe's Axe Mastery now uses a rank system
    Axe's Impact now uses a rank system
    Herbalism's Farmer's Diet now uses a rank system
    Herbalism's Green Thumb now uses a rank system
    Shake now uses a rank system
    Flux Mining now uses a rank system
    Removed traps from fishing
    Dodge now uses a rank system
    Arrow Retrieval now uses a rank system
    Axes' Critical Strikes now uses a rank system
    Axes' Greater Impact now uses a rank system
    Taming's Beast Lore now uses a rank system
    Green Thumb now uses a rank system
    Farmer's Diet & Fisherman's Diet now use a rank system

mcMMO Chat Alerts

    mcMMO no longer spams your chat!
    Most messages are sent to your action bar instead!
    Completely configurable! You can have mcMMO spam your chat again if you want!
    You can configure it so that messages will be sent to your action bar AND your chat system!
    Improved some of the messages sent to the player regarding the Chimaera Wing
    
Localization File
        
    The descriptions of a few skills have changed
    Locale files now support & codes for colors and formatting!
    Added locale strings for new Woodcutting abilities
    Added locale strings for mcchatspy command
    Added locale strings for JSON integration
    Added locale strings for Taming's Pummel SubSkill
    Added locale strings for Unarmed's Block Cracker SubSkill
    Removed localizations with the following codes for being almost empty: id, HR_hr, et_EE, lv, lt, no, pl_PL, pt_PT, tr_TR
    Removed redundant information from some skill names and descriptions en_US (other locales will need to be updated)
    SubSkill locale keys are now located at {ParentSkill}.SubSkill.SubSkillName
    Super Abilities no longer have (ABILITY) in their Skill.Effect strings
    
UI

    Certain elements of mcMMO's UI have been restyled
    Skills can now be clicked on and hovered over for more information!
    Added links to mcMMO related websites to various commands
    Customizeable and optional XP Bars
    Added the tagline "Overhaul Era" to various locations until 3.0.0 comes out
    Added option to disable the new URL links to config.yml
    
Sounds

    Volume and Pitch of sounds can now be configured in the new sounds.yml file
    
Super Ability Changes

    Skill Super Abilities now use a rank system, the default rank to unlock is level 5
    Activating Super abilities plays a sound (other plays can hear this)
    Ability Lengths now have a default skill cap at which they stop increasing in length
    Setting the cap to 0 removes it!
    Configurable in advanced.yml (endurance perks extend this limit)

Skills
    
    mcMMO now notifies you when you progress in a skill!
    Excavation Treasure Hunter is renamed to Archaeology
    Readying a tool for a super ability now plays a sound
    Skill Unlock Notifications have sounds
    Stripping wood and right clicking on stripped wood will no longer ready your Axe
    Added new skill 'Understanding The Art' which adds nothing new but tracks previously hidden benefits of raising a skill
    Tool alerts now are sent to the Action Bar
    Super Ability activation alerts are now sent to the Action Bar    
    Almost all Skill-related messages are now sent to the Action Bar    
    Added some missing information to skill stats
    Swords no longer require blocking with a shield to trigger counter attacks
    Sword's Bleed has been renamed to Rupture
    Sword's Rupture no longer has an internal hard coded limit
    Sword's Serrated Strikes now uses your Rupture rank to determine the damage/ticks for its bleed effect.
    Sword's Rupture now ticks four times as fast
    Sword's Rupture now refreshes bleed duration instead of adding duration when applying bleed to the same target
    Sword's Rupture will now deal lethal damage
    Sword's Rupture now reaches its max proc chance at level 20 (200 in Retro)
    Sword's Rupture now has a max chance to proc of 33% instead of 70%
    Sword's Rupture now deals 50% more damage at above Rank 3 and can last much longer! The base damage for Bleed has been increased as well (update your advanced.yml admins)
    Sword's Rupture no longer triggers invincibility frames when damaging your opponent
    Sword's Rupture now plays a sound
    Taming's Gore now uses Rupture Rank 1 for its DoT calculations
    Furnaces now give XP to the last person to modify their inventory instead of the first person to open them
    Rolling now plays a sound (Graceful Roll has a different sound :) )
    
    Acrobatics' Roll exploit detection was tweaked to still allow for Roll to trigger even if it rewards no XP
    Acrobatics' Roll & Gracefull Roll are now considered the same skill (both mechanics are still there)
    Some skill level rank requirements have changed
    
Experience
    
    Skills now start at level 1 (configurable in advanced.yml)
    Starting an XP event will now use the title API (toggle this in advanced.yml)
    The XP values of fish are now based on their rarity and have been drastically changed
    Coral (blocks) now give Mining XP
    Coral (plants) now give Herbalism XP
    Blue Ice now gives Mining XP
    Dolphins now give combat XP
    Drowned mobs now count towards combat XP
    Added missing mushroom blocks for XP
    You can now set guaranteed minimum values for XP gained if diminishing returns are enabled, this value defaults to 5% (experience.yml)
    
Bug Fixes

    Fixed the bug where mob names would be replaced by hearts
    Fixed a bug where Rupture would apply an incorrect amount of bleed ticks
    Fixed bug where XP rate could be a negative number
    Fixed a bug where you could set a players levels into the negative and bad things would happen
    Fixed an edge case bug where Blast Mining wouldn't inform the player that it was on cooldown
    
Plugin Compatibility

    mcMMO now fires new custom events relating to changes it makes to player scoreboards, plugin authors can listen to these events to improve compatibility
        
Exploit Fixes

    Prevented exploits involving blocks made from entities (snowmen, etc..)
    Chimaera Wing now tracks cooldowns between sessions for players (no more disconnect abuse)
    Tridents will no longer be considered unarmed
    
Parties

    Parties can now have size limits (configurable in config.yml), party size is unlimited by default
    You can now turn on Friendly Fire for parties in config.yml
    Party member list will only include members of the party that you can see (aren't vanished)
    
Scoreboards
    
    Scoreboards are now disabled by default since most of their functionality is handled better by XP bars.
    Added toggle to disable all scoreboards (previously you had to disable them one by one)
    You can turn them back on in config.yml
    You can have XP bars and scoreboards on at the same time
    
MySQL

    Added support for SSL for MySQL/MariaDB in config.yml (On by default)
    mcMMO no longer spams your console if you are not using SSL for your MySQL server
    You can now inspect offline players
    When converting from MySQL to flatfile mcMMO will now properly include all users in the conversion process
    
Admins
    
    Added ability for admins to spy on party chat (off unless toggled on) /mcchatspy
    The Debug stick can now tell you about properties of a block related to Excavation
    
API

    I've written a more detailed guide on API changes at http://api.mcmmo.org
    Added many missing SubSkills to SubSkillType class
    Moved a lot of methods from SkillCommand to SkillUtils
    SkillType is now PrimarySkillType
    SecondarySkill is now SubSkillType
    AbilityType is now SuperAbilityType
    SecondaryAbilityEvent is now SubSkillEvent
    SubSkillType has had many helpful methods added to it
    GREEN_THUMB_PLANT & GREEN_THUMB_BLOCK are replaced by GREEN_THUMB
    
Permissions

    Removed all mob health bar permissions, this is no longer a per-player setting.
    Added permission node mcmmo.commands.mcchatspy & mcmmo.commands.mcchatspy.others
    Added mcmmo.commands.mmoinfo for the new mmoinfo/mcinfo command
    Added permission nodes for Harvest Lumber, Splinter, Nature's Bounty, and Bark Surgeon
    Call of the wild now uses mcmmo.ability.taming.callofthewild instead of mcmmo.ability.taming.callofthewild.all
    Replaced the old Double Drop permission node for woodcutting with a new Harvest Lumber permission node
    Fast Food Service permission node renamed to mcmmo.ability.taming.fastfoodservice
    Counter Attack permission node renamed to mcmmo.ability.swords.counterattack
    Arrow Deflect permission node renamed to mcmmo.ability.unarmed.arrowdeflect
    Iron Arm Style permission node renamed to mcmmo.ability.unarmed.ironarmstyle
    
Commands

    Added new info command /mmoinfo or /mcinfo
    Added toggle command /mcchatspy
    '/mcMMO help' no longer displays the other/special commands category to players lacking permissions
    Removed the mobhealthbar command, this is no longer a per-player setting.
    
Misc Config Changes

    Removed SkillShot's IncreaseLevel & IncreasePercentage (replaced by RankDamageMultiplier)
    Removed AxeMastery's MaxBonus & MaxBonusLevel (replaced by RankDamageMultiplier)
    Unarmed.IronArm in advanced.yml is now Unarmed.IronArmStyle
    Unarmed.Deflect in advanced.yml is now Unarmed.ArrowDeflect
    Swords.Counter in advanced.yml is now Swords.CounterAttack
    Archery.Retrieve in advanced.yml is now Archery.ArrowRetrieval
    Axes.CriticalHit in advanced.yml is now Axes.CriticalStrikes
    Archery's Skill Shot now uses RankDamageMultiplier for its damage bonus calculations
    Axe's Axe mastery now uses RankDamageMultiplier for its damage bonus calculations
    
Misc Changes

    Removed everything involving the kraken
    Code cleanup in a lot of places... unfortunately there is still much left to do!
    
///////////////////////////////    

EVERYTHING BELOW HERE IS OLD AND KEPT FOR HISTORICAL PURPOSES AND FORMATTED DIFFERENTLY

//////////////////////////////

Key:

    + Addition
    = Fix
    ! Change
    - Removal
  

Version 2.0.0

 = Fixed an interaction between Tree Feller and Stripped Wood
 ! Fireworks no longer fire by default for ability activation/deactivation
 ! Website has been changed and the MOTD string relating to it reflects this
 ! Discord link added to mcMMO command
 ! Updated misc strings relating to mcMMO


Version 1.5.05-SNAPSHOT

Version 1.5.04
 + Added option to config.yml to control mcMMO generated sound volume
 + Added option to config.yml to truncate existing player skill levels that exceed the skill level cap
 + Falling blocks persist mcMMO natural data
 = Woodcutting double drops correctly identify acacia and dark oak logs
 = Skill Reset command now correctly identifies arguments
 = Hylian Treasure config options are now actually used
 = Child skills now use parent skills configured skill caps properly
 = Auto Update config now properly works
 ! Item dropped from blocks now drop from the center
 ! Potions Config updated for 1.9
 ! Flux mining now simulates a block break event for other plugins to act upon
 ! Zombie Pigmen spawned from nether portals are now considered spawner mobs
 ! Flux Pickaxe lore now appends to existing lore as opposed to replacing it
 ! Party chat no longer displays colors when logged in server console
 - Treefeller no longer lowers exp for big trees
 - No longer supports 1.8 :(
 - Removed plugin metrics

Version 1.5.03
 = Fixed bug where absorption hearts could be attacked by allied players
 = Fixed bug where new forms of stone would drop the wrong type when mined with Silk Touch
 = Fixed bug where blocks would not get tracked correctly when using sticky pistons and slime blocks in certain situations
 = Fixed bug where config value for Daze damage was ignored
 = Fixed UUID updater to not lose data on errors
 = Fixed bug where uuid update could result in large amounts of user data being deleted
 = Fixed bug where custom potions were missed in potion stage calculation
 = Fixed piston dupe bugs permanently
 = Fixed bug involving user name changes
 = Fixed old user purge to properly calculate months
 = Fixed bug where Repair would incorrectly check items
 = Fixed bug where apostrophes in locale files would not read correctly
 = Fixed bug where treasure data was limited to 255 instead of Short.MAX_VALUE
 ! Moved more user loading calculations to async loading thread to reduce lag on login

Version 1.5.02
 + Added option to config.yml for Chimaera Wings to stop using bed spawn points
 + Added option to config.yml to let non-tools in hand count as unarmed
 + Added option to experience.yml to control XP gained by killing bred animals
 + Added support for 1.8 mobs and features
 = Fixed bug where no Mining XP was granted when Flux Mining was successful
 = Fixed bug with UUID conversions in Flatfile
 = Fixed a couple Dupe bugs that were introduced recently
 = Fixed bug where MobHealthbarTypes were not saved between server restarts
 ! Changed Flux Mining mechanics. In order to use the ability, you need to infuse a pickaxe with furnace powers first.
 ! Scoreboard tips are only shown a couple of times to the player, instead of once per login session
 ! Changed Archery distance multiplier to be configurable
 ! Archery distance XP bonus cannot exceed indefinitely anymore

Version 1.5.01
 + Added new child skill; Salvage
 + Added UUID support!
 + Added SQL connection pooling and async loading!
 + Added the long awaited Diminished Returns feature
 + Added new feature to Herbalism. Instantly-regrown crops are protected from being broken for 1 second
 + Added option to config.yml to show the /mcstats scoreboard automatically after logging in
 + Added option to config.yml for Alchemy. Skills.Alchemy.Prevent_Hopper_Transfer_Bottles
 + Added option to config.yml for Scoreboards, display "Ability" instead of ability names on the scoreboards
 + Added options to experience.yml for Dirt and Sand variations
 + Added support for `MATERIAL|data` format in treasures.yml
 + Added API to experience events to get XP gain reason
 + Added API to check if an entity is bleeding
 + Added API to ExperienceAPI to get the amount of XP needed for a level
 + Added API class SkillAPI used to get a list of valid skill names
 + Added API events for hardcore features, McMMOPlayerPreDeathPenaltyEvent, McMMOPlayerStatLossEvent and McMMOPlayerVampirismEvent
 + Added API to ExperienceAPI to specify if XP can be shared
 + Added options to tools.yml and armor.yml config files to set a pretty repair material name
 + Added full support for repairables in tools.yml and armor.yml config files
 + Added magical mod config file import command, for Cauldron 1.7+. Check wiki for usage
 + Added particle effects and sounds to "Call of the Wild" (Taming)
 + Added summon length to "Call of the Wild". Summons will now commit suicide after their lifespan expires
 + Added feature which makes tamed wolves attack a target shot by the owner
 = Fixed bug where pistons would mess with the block tracking
 = Fixed bug where the Updater was running on the main thread.
 = Fixed bug when players would use /ptp without being in a party
 = Fixed bug where player didn't have a mcMMOPlayer object in AsyncPlayerChatEvent
 = Fixed bug where dodge would check the wrong player skill level
 = Fixed bug which causes /party teleport to stop working
 = Fixed bug where SaveTimerTask would produce an IndexOutOfBoundsException
 = Fixed bug where Alchemy would not fire BrewEvents
 = Fixed bug with setting custom names and lore in treasures config
 = Fixed bug which would cause a NullPointerException with getFlowerAndGrassXp()
 = Fixed bug which could cause and SQLException regarding the connection property 'maxReconnects'.
 = Fixed bug where falling blocks were incorrectly tracked
 = Fixed bug where items would get deleted when in Berserk with a full inventory
 = Fixed bug where the console would not correctly show party chat colors
 = Fixed bug where party chat was using non thread safe methods
 = Fixed bug where Blast Mining unlock levels could be to high in certain occasions
 = Fixed bug where Blast Minings ability "Demolition Expert" would not work
 = Fixed bug where Repair_Material_Quantity wasn't read in mod config files
 ! Changed SecondaryAbilityEvent to implement Cancellable and it now gets fired for damage related secondary abilities
 ! Changed the way mcMMO handles bonus damage, updated for the new damage event API
 ! Changed player data saving. Save tasks are now asynchronous
 ! Vanished players no longer get hit by AoE effects
 ! Changed Alchemy config option 'Prevent_Hopper_Transfer' renamed to 'Prevent_Hopper_Transfer_Ingredients'
 ! Changed Alchemy XP distribution. XP is granted based on the stage of the potion.
 ! Changed behavior of the Blast Mining ability "Demolition Expert"; now only decreases damage for the ability user
 ! Updated for new getOnlinePlayers() behavior
 ! Updated for new blocks and entities
 ! Changed McMMOPlayerDeathPenaltyEvent to get fired after hardcore penalty calculations, use McMMOPlayerPreDeathPenaltyEvent for old behavior
 ! Moved Refresh_Chunks setting from hidden.yml to config.yml
 - Removed salvage ability from Repair, salvage has it's own (child) skill now

Version 1.5.00
 + Added Podzol & Red Sand to Excavation
 + Added Hardened Clay, Stained Clay, and Packed Ice to Mining blocks
 + Added Acacia and Dark Oak to Woodcutting blocks
 + Added Salmon, Clownfish, and Pufferfish to Fishing XP
 + Added new flowers and grasses to Herbalism XP
 + Added option to config.yml which allows players to always catch fish, even when a treasure is found
 + Added option to config.yml to override vanilla Minecraft treasures
 ! Fishing XP now depends on the type of fish.
 ! Woodcutting XP in experience.yml and Woodcutting double drops in config.yml now use the tree species names. Oak is now Generic, and Spruce is now Redwood.
 ! Red_Rose was replaced by Poppy, and so the key in experience.yml has been updated accordingly.
 - Removed deprecated permission nodes
 - Removed "Treasure found!" message

Version 1.4.08
 + Added a new skill; Alchemy. Special thanks to EasyMFnE for creating this!
 + Added SecondaryAbilityType enum, and new SecondaryAbilityWeightedActivationCheckEvent, fired when a secondary ability checkes its activation chances
 + Added the possibility to gain experience when using Fishing "Shake"
 + Added config options to disable various sound effects
 + Smelting now works with custom ores - add smelting XP value to blocks.yml, or it will default to 1/10th of normal XP.
 + Added automatic cleanup of backups folder.
 + Added bypass permission for finding Fishing traps
 + Added level threshold settings to hardcore modes. When a players skill level is below this threshold, they will not lose any stats
 + Added party alliances, two parties can now team up. Allies share party chat and cannot harm each other.
 + Added new experience bonus perk 'mcmmo.perks.xp.10percentboost.<skillname>' multiplies incoming XP by 1.1
 + Added new experience bonus perk 'mcmmo.perks.xp.customboost.<skillname>' multiplies incoming XP by the boost amount defined in the experience config
 + Added Ender Dragon, Wither, and Witch to combat experience multipliers - they do not give XP by default
 + Added support for multiple mod config files, naming can be done as either armor.<modname>.yml or <modname>.armor.yml
 + Added config options to configure the items used in "Call of the Wild"
 + Added config option to configure the database command cooldown
 = Fixed bug where healthbars wouldn't display if skills were disabled
 = Fixed bug with "Call of the Wild" entities despawning
 = Fixed bug with updating (very) old user data.
 = Fixed bug with checking maximum durability of mod items.
 = Fixed exploit involving Call of The Wild.
 = Fixed bug where LeafBlower permissions were ignored
 = Fixed bug with toggle commands not properly displaying the success message.
 = Fixed IllegalArgumentException caused by an empty Fishing treasure category
 = Fixed bug with Salvage not reading the config value for the anvil material.
 = Fixed exploit where you could receive smelting XP for improper items
 = Fixed bug where the Unbreaking enchantment was ignored when using "Super Breaker" or "Giga Drill Breaker"
 = Fixed bug which prevented players from gaining Acrobatics XP when the setting 'Prevent_XP_After_Teleport' was set to false
 = Fixed bug where cooldown donor perks were reducing more than expected
 = Fixed bug where disabling hardcore mode for specific skills didn't work
 = Fixed bug which caused the backup cleanup to delete old backups while it should have kept those
 = Fixed bug where party chat broke if the display name contained special characters
 = Fixed bug where `/addlevels all` and `/skillreset all` didn't work
 = Fixed bug which made it possible to gain XP by taming the same horse multiple times, if a player "untamed" that horse
 = Fixed bug where some horses summoned with "Call of the Wild" were unable to jump
 = Fixed bug where the /ptp request expiration time was checked wrongly - preventing players from using the command
 = Fixed bug where Hylian Luck was broken
 = Fixed bug where Snow would never drop treasures
 = Fixed issues with commands giving away vanished players.
 = Fixed bug where the Repair lucky perk would increase the Arcane Forging downgrade chance, instead of decreasing it
 ! Changed party system. Parties now have XP and Levels. Party features such as party teleport and party chat have to be unlocked before they can be used by the party members
 ! Changed appearance of party member list. Gold = party leader, White = online, Gray = offline, Italic = not nearby
 ! Updated localization files
 ! Changed the appearance of /mcmmo commands
 ! Changed AxesCritical to CriticalHit in config file
 ! Changed several secondary ability permissions(deprecated versions still exist)
 ! Changed /ptp config setting, Commands.ptp.Confirm_Required is now Commands.ptp.Accept.Required
 ! Changed config validation for UnlockLevels, they can now also be 0
 ! Changed config validation for Rank_Levels, successive Ranks can now be less than or equal to each other
 ! Changed default amount of XP gained from mining Quartz Ore. From 250 to 100 XP.
 ! Changed Acrobatics config setting, Skills.Acrobatics.Prevent_XP_After_Teleport is now Skills.Acrobatics.XP_After_Teleport_Cooldown
 - Removed /stats alias for /mcstats

Version 1.4.07
 + Added XP boost to Acrobatics when wearing Boots of Feather Falling
 + Added SQL Database can now recover from a dropped connection without losing data. (Thanks Riking!)
 + Added more tiers to Fishing, Repair and Smelting!
 + Added Carrot on a Stick and Flint & Steel to repair.vanilla.yml
 + Added horses to the "Shake" ability
 + Added ability to summon horses via "Call of the Wild" using apples
 + Added XP gain to Taming for horses
 + Added new permission nodes to allow more control over Taming and "Call of the Wild"
 + Added new experience.yml config file! Moved all experience related settings from config.yml to experience.yml
 + Added support for EXPONENTIAL formula curves to experience.yml
 + Added new /mcconvert command to convert players levels and experience from one formula curve to another.
 + Added snow to Excavation blocks
 + Added new experience curve option. Cumulative curve, calculates experience needed for next level using power level.
 + Added extra settings to config.yml for "Call of the Wild" (Taming)
 + Added a 5 second cooldown after teleporting before Acrobatics XP can be earned. Plus a config option to disable
 + Added new API methods to ExperienceAPI to get a players rank on the leaderboards
 + Added new McMMOPlayerDeathPenaltyEvent, fired when a player dies and would lose levels
 + Added new McMMOPlayerLevelChangeEvent, fired when a players level changes
 + Added new McMMOPlayerLevelDownEvent, fired when a player loses levels
 + Added ability to give custom names to items in treasures.yml - use the key "Custom_Name" to set, expects a string.
 + Added ability to give lore to items in treasures.yml - use the key "Lore" to set, expects a list of strings.
 + Added Quartz and Name Tags to the default Excavation treasures
 + Added a warning message if the server is running NoCheatPlus without CompatNoCheatPlus
 + Added cooldown to commands with heavy database access to prevent denial of service
 + Added /mcscoreboard keep, to keep the scoreboard up forever
 + Added Rainbow Mode to scoreboards
 + Added new /mccooldowns command to show all ability cooldowns
 + Commands may now both print text and display a scoreboard
 + Killing a custom entity will automatically add it to the custom entity config file with default values.
 = Fixed bug which allowed players to bypass fishing's exploit prevention
 = Fixed bug where FakeEntityDamageByEntityEvent wasn't being fired
 = Fixed bug with "Skull Splitter" not finding the locale string
 = Fixed issue where locale strings could cause the scoreboard header to be longer than 16 characters.
 = Fixed a bug with "Beast Lore" when the entity had no owner but was tamed.
 = Fixed a bug where AbilityDeactivateEvent would throw an error if the player logged out before his ability ran out.
 = Fixed a bug where LevelUpEvent would be called for an offline player.
 = Fixed a bug where teleport location was never reset if warmup was set to 0 for "Chimaera Wing".
 = Fixed a bug where the "Dodge" DamageModifier wasn't being read from advanced.yml
 = Fixed a bug where squid were not awarding XP.
 = Fixed a bug where Combat XP was granted within 5 seconds for respawned players
 = Fixed a bug where wrong feedback messages were being send when using a command on an offline player
 = Fixed a bug where players were able to gain Herbalism XP in mine carts, even though Prevent_AFK_Leveling was enabled
 = Fixed a bug where players would get hit by fireworks if they leveled up while in a boat
 ! Changed Fishing "Treasure Hunter" and "Magic Hunter" drop percentages
 ! Changed format of mod config files. (blocks.yml, tools.yml, armor.yml and entities.yml) **YOU WILL NEED TO UPDATE YOUR FILE TO THE NEW FORMAT**
 ! Changed format of treasures.yml. **YOU WILL NEED TO UPDATE YOUR FILE TO THE NEW FORMAT**
 ! Changed format of repair.vanilla.yml. **YOU WILL NEED TO UPDATE YOUR FILE TO THE NEW FORMAT**
 ! Changed default XP multiplier for repairing shears
 ! Changed "Shake" drops for Witches. They no longer drop water bottles, since they no longer drop them in Vanilla.
 ! Changed fishing exploit prevention, by default it will no longer send global sounds, effects and messages.
 ! Changed Hardcore modes, they will also subtract experience
 ! Changed various values to double in advanced.yml for the sake of consistency.
 ! Nerfed Fishing "Master Angler" (removed skill level based bonus) and also made the modifiers configurable
 ! Nerfed Archery damage to eliminate constant one-hit kills.
 ! Changed the way Repair hands out XP, also added config options to control Repair XP
 ! Changed Swords "Counter Attack" ability from passive to active. Blocking is required to activate.
 ! Hardcore modes can now be toggled for each skill individually
 ! Vampirism can now be enabled without having Skill Death Penalty enabled
 ! Admin and Party chat prefixes are now customizable
 ! Changed the color of party leader names in Party chat
 ! Improved "Tree Feller" algorithm (Thanks Riking!)
 ! Improved AFK Acrobatics prevention mechanism
 ! Improved profile saving
 ! Improved partial name matcher
 ! Improved update checker
 ! Updated localization files
 ! Party item share category states are now saved when the server shuts down.
 ! When using "Super Breaker" or "Giga Driller" abilities extra tool durability is used (again)
 ! Mob healthbars are automatically disabled when the plugin "HealthBar" is found
 ! Massively improved scoreboard handling
 ! Reworked scoreboard configuration (config.yml) - **you will need to update**
 - The /mmoupdate command has been removed. It is replaced by /mcconvert database
 - Removed Abilities.Tools.Durability_Loss_Enabled, set Abilities.Tools.Durability_Loss to 0 to disable instead.
 - Removed Skills.Fishing.Shake_UnlockLevel from advanced.yml, now using Skills.Fishing.Rank_Levels.Rank_1 instead.
 - Removed SpoutPlugin support

Version 1.4.06
 + Added "Ice Fishing" ability to Fishing
 + Added global scoreboards to track skill rankings (display using /mctop)
 + Added per-player scoreboard displays for the /inspect, /mcrank, /mcstats, and /<skillname> commands
 + Added tab-complete support for all commands
 + Added ability to configure drops from Shake in treasures.yml
 + Added "Master Angler" ability to Fishing.
 + Added health display for mobs during combat.
 + Added new API method to McMMOPlayerLevelUpEvent to set levels gained
 + Added new permission node for /ptp; mcmmo.commands.ptp.send (enabled by default)
 + Added configurable cooldown and warmup times when using /ptp
 + Added a new Party item share category "Misc" which contains a list of configurable items. (By default all tools and armor)
 + Added fishing exploit prevention
 + Added permission node to bypass the fishing exploit prevention
 + Added boosts to Fishing chance depending on conditions
 + Added McMMOAbilityActivateEvent and McMMOAbilityDeactivateEvent
 + Added config option to toggle the size of fireworks
 + Added config option to multiply xp gains from mob spawner mobs
 + Added multiplier to Archery XP based on bow force
 + Added information about /party itemshare and /party expshare to the party help page
 + Added option to use scoreboards for power level display instead of Spout.
 + Added permission node to prevent inspecting hidden players
 + Added SQL to Flatfile database conversion
 + Added ability to use custom database managers and convert to/from them
 = Fixed bug which could cause the server to hang for a minute when checking for updates. (Thanks to Riking)
 = Fixed bug where spawned arrows could throw ArrayIndexOutOfBoundsException
 = Fixed bug where custom Spout titles were overwritten by mcMMO.
 = Fixed bug where Nether Quartz wasn't included in Smelting or item sharing
 = Fixed bug where players were able to join the same party multiple times
 = Fixed displaying partial names when trying to use /ptp
 = Fixed wolves from Call of the Wild only having 8 health
 = Fixed bug where /party chat was not working
 = Fixed bug where experience commands were adding levels to all skills when they shouldn't
 = Fixed mcmmo.commands.ptp.send not being set by default
 = Fixed NPE when trying to tab-complete /mctop
 = Fixed Fishing treasures always having the same enchants
 = Fixed Smelting returning ink sacs instead of Lapis when double-dropping
 = Fixed bug where players could remain in party chat after leaving or being kicked from a party.
 = Fixed bug where non-player arrows couldn't be deflected.
 = Fixed experience being applied even when the permission for a skill was denied
 = Fixed possible item duplication bug with infinity bows
 = Fixed bug with removing players from mySQL database
 = Fixed bug with empty metadata lists and Smelting
 = Fixed bug where Blast Mining would drop wrong items
 = Fixed bug with Blast Mining where the Ability refreshed message was being send too early
 = Fixed bug where the chance of a successful Gracefull Roll was twice as high as displayed
 = Fixed bug where lucky perks where not working
 = Fixed bug with Ice Fishing on a single block of ice
 = Fixed bug with Ice Fishing which allowed players to break ice in protected areas
 = Fixed a small bug with mob healthbars and bosses, such as EnderDragons and Withers
 ! Changed Spout notification tiers to be stored in SpoutConfig instead of AdvancedConfig
 ! Changed Berserk to add items to inventory rather than denying pickup
 ! Changed Call of the Wild, newly summoned pet's will have a custom name. (added permission node to disable this)
 ! Changed Chimaera Wing's recipe result to use the ingredient Material
 ! Changed Repair to ask a confirmation of the player when he tries to repair an enchanted item
 ! Players will no longer pickup items to their hotbar while using Unarmed
 ! ExperienceAPI methods will now throw InvalidSkillException if the skill name passed in is invalid.
 ! Changed default value for recently-hurt cooldown between teleports, this is also fully configurable now
 ! Changed the amount of info messages in the console when enabling/disabling, enable Verbose_Logging to enable them again
 ! Items dropped by players are now being tracked and are not being shared with party members
 ! Optimized tracking of tool & ability cooldowns.
 ! Updated the localization files

Version 1.4.05
 + Added option to allow refreshing of chunks after block-breaking abilities. (Disabled by default)
 + Added fireworks effects when a player levels-up, for every 100 levels (configurable)
 = Fixed bug where /addxp was setting instead of adding experience
 = Fixed bug where /addxp was not processessing level-ups for online players
 = Fixed bug which allowed players to share experience with nearby dead players
 = Fixed bug with ChimaeraWings not taking Wings from a players inventory properly
 = Fixed bug which caused a NPE when trying to use /mctop smelting
 = Fixed Berserk misbehaving when /reload was used
 = Fixed parties misbehaving when /reload was used
 = Fixed Berserk getting "stuck" when /mcrefresh was used
 = Fixed ClassCastException with Taming
 = Fixed huge mushroom blocks not being properly tracked
 = Fixed potion buff option not using the appropriate # of ticks
 = Fixed Chimera Wing spamming console if Metrics was disabled
 = Fixed Chimera Wing displaying warmup message if warmup was set to 0
 = Fixed party & admin chat errors when not aysnc
 ! Updated localization files

Version 1.4.04
 + Added functions to ExperienceAPI for use with offline players
 + Added Nether Quartz Ore to Mining
 + Added Dropper, Hopper, and Trapped Chest to blocks that shouldn't activate abilities
 + Added partial name matching
 = Fixed bug where trying to activate a Chimaera Wing would require one item too much
 = Fixed bug where Treefeller would try to cut too many leaves and reach the threshold when it shouldn't
 = Fixed bug where Mining wasn't awarding double drops
 = Fixed bug where Shake wouldn't damage mobs whose max health was less than 4
 = Fixed bug where the API would fail if the name of a player's current party is requested when the player isn't in one (Thanks @dualspiral!)
 = Fixed bug with retrieving a player's party members
 = Fixed bug which caused a NPE when trying to join the party of a non-existing player or when ptp to a non-existing player
 = Fixed bug which causes a NPE when trying to use /mcrefresh from the console
 = Fixed bug where Carrots and Potatoes weren't awarding Herbalism XP.
 = Fixed bug where some herbalism drops weren't properly shared within parties.
 = Fixed bug where players wouldn't be able to pick up items if they logged our while Berserk was still active.
 ! Changed config node name for the skill experience modifiers from "Experience.Formula.Multiplier.[Skill]" to "Experience.Formula.Modifier.[Skill]"
 ! Updated localization files
 ! mcMMO abilities can no longer be activated while in Creative mode
 ! Expanded ChatAPI to allow toggling of chat states for users
 ! Updated to EMetrics 0.0.4-SNAPSHOT
 - Removed deprecated functions from API classes.
 - Removed functions for getting the PlayerProfile - using API classes is preferred, but if not the McMMOPlayer should be used instead
 - Removed Ender Dragon, Wither, and Witch from granting combat experience and related configuration options

Version 1.4.03
 + Added option to advanced.yml to determine the # of enchant levels used when buffing Super Breaker & Giga Drill Breaker
 + Improved stats display for child skills
 + Added cooldown between using Chimaera Wings
 = Fixed bug with '/party chat (on|off)' and '/partychat (on|off)' not working
 = Fixed bug with Repair not decreasing enchanting levels properly
 = Fixed bug with Smelting not properly tracking furnaces
 = Fixed bug with Blast Mining not dropping blocks correctly
 = Fixed bug with custom blocks not working
 = Fixed bug with Blast Mining increasing TNT damage.
 = Fixed bug where Blast Mining was awarding too much XP
 = Fixed bug where triple drops would award twice the amount of experience in Herbalism and Mining
 = Fixed bug where Green Thumb would consume wheat instead of seeds
 = Fixed bug where Green Terra would consume twice the amount of seed when used on crops
 = Fixed bug where experience would be awarded in Herbalism for some player-placed blocks
 = Fixed bug where players were unable to salvage leather armor
 = Fixed bug with repairing using materials with byte metadata
 = Fixed bug where Fishing was becoming less successful at higher levels
 = Fixed bug with using Salvage on stacked items.
 = Fixed bug where the 'mcmmo.commands.ptp.world.all' was registered twice
 = Fixed bug where Beast Lore wouldn't work on friendly pets
 = Fixed bug where Deflect was calculated based on the attacker, not the defender. (We really did this time!)
 = Fixed bug where Treefeller would not deal durability damage when the axe "splinters into dozens of pieces"
 ! Moved the Salvage unlock level from config.yml to advanced.yml
 ! Changed how Chimaera Wings are acquired, you need to craft them now. (By default, use 5 feathers in a shapeless recipe)
 ! Changed how Chimaera Wings teleport players to the spawnpoint, will now check if the location is safe
 - Removed option to disable Salvage via the config file. This should be handled via permissions instead.
 - Removed the option to use Woodcutting without an axe from the config file.

Version 1.4.02
 + Added API to get the skill and power level caps.
 = Fixed bug where Deflect was calculated based on the attacker, not the defender
 = Fixed bug where some skills weren't registering as unlocked until one level later
 = Fixed bug where the PTP cooldown was being read improperly
 = Fixed bug where /ptp <accept|toggle|acceptall> where broken
 = Fixed ClassCastException relating to counter-attack with Swords
 = Fixed issue with some skill activations not activating enough or activating too much

Version 1.4.01
 = Fixed bug where trying to use /mctop or /xplock with the Smelting child skill caused NPEs
 = Fixed bug where /mctop and /mcrank wouldn't show overall power levels for servers using Flatfile
 = Fixed bug where Smelting would throw consistent errors due to offline players
 = Fixed bug where repairing an mcMMO ability-buffed item with mcMMO repair could take the enchant but leave the lore tag
 = Fixed bug where using '/party chat message...' would result in the first word of the message being printed repeatedly
 = Fixed bug where the wrong flag was being set when taking damage
 = Fixed bug where the PTP cooldown was set improperly
 = Fixed bug where ptp permissions weren't being handled properly
 = Fixed bug where Beast Lore wouldn't work
 = Fixed bug where Chimaera Wing would always teleport to spawn, even when the player had a valid bed spawn location
 = Updated locale files

Version 1.4.00
 + Added new Child Skill - Smelting!
 + Added a version check, admins will get notified when a new version is available!
 + Added new cancellable McMMOPlayerDisarmEvent for Citizens compatibility - fires whenever a player is disarmed.
 + Added config options for Hylian Luck skill
 + Added display values to Unarmed command for Iron Grip
 + Added '/party create <name>' command, use this to create a party
 + Added '/party disband' command, kicks out all members and deletes the party
 + Added '/ptp toggle' command, to disable party teleportation.
 + Added '/ptp accept' and '/ptp acceptall' commands
 + Added an automatic party kick when a party member has been offline for 7 days (default)
 + Added a permission to allow friendly fire in parties, both attacker and defender must have it for friendly fire to occur
 + Added timeout on party teleport requests
 + Added XP bonus for Archery based on distance from shooter to target
 + Added ability to config Hylian Luck drops through treasures.yml
 + Added party XP sharing, when more party members are near the share bonus increases.
 + Added vanilla XP boost for Fishing - includes permissions, config options, etc
 + Added particle effect for bleeding
 + Added methods to check if a player is in party or admin chat to the ChatAPI
 + Added /mcpurge functionality for Flatfile users
 + Added basic support for Mo' Creatures (and other entity mods) - specify mob info in entities.yml
 + Added Shears, Buckets, Fishing Rods, Flint & Steel, Carrot Sticks, and Bows to the list of items that can be Salvaged
 + Added the "wait" music disc to the default fishing treasures
 + Added "Chinese (Taiwan)" localization files (zh_TW)
 + Added '/hardcore' and '/vampirism' commands for toggling these modes on or off.
 + Added Block Cracker to Unarmed's Berserk, turn smooth brick into cracked smooth brick
 + Added config option to disable automatic zip backups.
 + Added particle effects for many abilities.
 + Added '/mcnotify' command to toggle ability notifications on/off
 + Added ability for config files to automatically update with new keys, and prune out old ones
 + Added config option to make .new config files instead over writing over old ones when updating
 + Added "Holy Hound" ability to Taming
 + Added "Shroom Thumb" ability to Herbalism
 + Added child.yml config file to choose parents for child skills
 + Added '/party itemshare <NONE | EQUAL | RANDOM>' command to choose party item share mode
 + Added '/party itemshare <loot | mining | herbalism | woodcutting> <true | false>' command to control items that are shared
 + Added itemweights.yml file to determine which items are more valuable for party itemshare
 = Fixed Green Thumb on wheat not working properly at rank 4
 = Fixed Green Thumb and Green Terra consuming twice the amount of seed needed
 = Fixed Green Terra not also checking Green Thumb permissions
 = Fixed bug where splash potions could raise a player's unarmed level
 = Fixed bug where fired arrows could raise skill levels other than Archery
 = Fixed /ptp telporting the target to the player, rather than the other way around.
 = Fixed Impact reducing the durability of non-armor equipped blocks
 = Fixed Impact reducing improperly the durability of armors (as a consequence it is now more effective)
 = Fixed multiple commands not working properly on offline players
 = Fixed /mmoedit not giving feedback when modifying another players stats
 = Fixed the guide usage string showing up every time /skillname was called
 = Fixed Spout not being able to precache our resources properly, and therefore making our XP bars fail
 = Fixed Spout config files loading / generating when they shouldn't have
 = Fixed mod config files loading / generating when they shouldn't have
 = Fixed bug where Green Terra could activate on crops that weren't fully grown.
 = Fixed several typos relating to locale string display
 = Fixed bug where all skill guide headers appeared as "Skillname Guide Guide"
 = Fixed bug where Impact was applied incorrectly due to an inverted method call
 = Fixed bug where Impact improperly determined the defender's armor
 = Fixed a bug which made it impossible to join other players' parties
 = Fixed ArrayIndexOutOfBoundsException resulting from being unranked in a skill when using FlatFile
 = Fixed Woodcutting accidentally using Mining double drop values.
 = Fixed Hylian Luck not removing the block-placed flag from flowers.
 = Fixed Hylian Luck not checking the block-placed flag on flowers.
 = Fixed Leaf Blower not respecting the unlock level set in advanced.yml
 = Fixed abilities activating with the wrong tool in hand
 = Fixed Experience.Gains.Mobspawners.Enabled not being used correctly (the check was inverted)
 = Fixed bug where Iron Grip was using the attacker's skill values rather than the defender's.
 = Fixed a bug where /party kick would trigger the PartyChangeEvent for the wrong player
 = Fixed /party kick not working on offline players
 = Fixed a bug where party join messages weren't displayed
 = Fixed a bug where a new party leader wasn't appointed, after the previous party leader left
 = Fixed a bug where Disarm and Deflect had wrong values
 = Fixed Magic Hunter (Fishing ability) favoring certain enchants
 ! Changed our custom chat events to be async
 ! Changed some config value key names regarding double drops and XP - make sure you copy any custom values to your new config after updating.
 ! Changed Green Terra blocks to be determined via permissions instead of the config file
 ! Config files are now backed up even when running in SQL mode
 ! Changed /p and /a to use /partychat and /adminchat as the default command name. The use of /p, /pc, /a, and /ac is still supported.
 ! We're now using Bukkit sounds instead of Spout sounds.
 ! It is now possible to use a negative number for Max_Level in treasures.yml to not use a maximum level, changed default file accordingly
 ! A Fishing catch will now always contains a fish even if a treasure is found
 ! Changed how Berserk handles not picking up items to avoid listening to PlayerPickupItemEvent
 ! Moved Hylian Luck into a separate listener since it actually cancels the event and shouldn't just be on MONITOR.
 ! Changed how Tree Feller is handled, it should now put less stress on the CPU
 ! Changed Tree Feller to work on huge mushrooms
 ! Changed Fisherman's Diet and Farmer's Diet to use two seperate config values
 ! Major refactoring - please take note, this WILL break any mcMMO-related plugin not properly hooking into the API.
 ! Changed the way party commands work, use /party ? to check how to use the new commands
 ! Changed McMMOChatEvent to contain the plugin that the event originated from.
 ! Changed Excavation to have individual XP values for each block type, rather than a base XP value.
 ! Changed the way party teleportation works. When using /ptp, the target player needs to confirm the teleport before it takes place. (Configurable)
 ! Changed BeastLore: Now also displays offline player names
 ! Changed backup task to include ALL config files
 ! Deprecated most functions in ExperienceAPI, replaced them with identical versions that use a String for the SkillName rather than the SkillType enum values
 ! Changed Super Breaker & Giga Drill Breaker to be an enchantment-based boost, rather than an instabreak. Option exists in hidden.yml to change this to an potion-based buff.
 ! Changed locales to fall back on English when translated strings cannot be found.
 - Removed Party "master/apprentice" system. Replaced with the new party XP share feature.
 - Removed unused "healthbar" files from the resources
 - Removed config options for disabling commands from the config.yml. This should instead be done through permissions.
 - Removed /mcc command. Replaced with /mcmmo [?|help|commands]
 - Removed options to allow Mining & Excavation without a tool due to the changes to their abilities

Version 1.3.14
 + Added new Hylian Luck skill to Herbalism.
 = Fixed a memory leak involving mob tracking
 - Removed extra durability loss from Leaf Blower

Version 1.3.13
 + Added task & command to prune old and powerless users from the SQL database.
 + Added Craftbukkit 1.4.6 / 1.4.7 compatibility
 + Added new /mcrank command for showing a players leader board ranking for all skills in one place
 + Added a configurable durability cap for ArmorImpact to advanced.yml
 + Added the version number to /mcmmo
 + Added bats, giants, witches, withers, and wither skeletons to the mcMMO combat experience list, and makes their experience drops configurable
 + Added the ability to track mobs spawned by mob spawners or the Taming ability when the chunks they are in unload and reload
 + Added wooden button to the list of items that shouldn't trigger abilities
 + Added a new feature to fishing. Players will have +10% chance of finding enchanted items when fishing while it's raining
 + Added displaying bonus perks on skill commands
 + Added config option to disable gaining Acrobatics XP from dodging lightning
 + Added missing skill guides. They're finally here!
 + Added more localization 
 + Added a very secret easter egg
 = Fix issue with Sand/Gravel tracking
 = Fix possible NPE when using the PartyAPI to add a player to a party that doesn't exist.
 = Fix mcremove command for mySQL
 = Fix a java.io.FileNotFoundException when using SQL
 = Impact now works with mobs wearing armor
 = Fixed issue with Tree Feller dropping player-placed blocks
 = Fixed issue with missing default cases from several switch/case statements
 = Fixed issue with Mining using actual skill level rather than max skill level
 = Fixed some issues with static access
 = Fixed ItemStack deprecation issues
 = Fixed Async deprecation issues
 = Fixed a bug with MySQL databases (non-alphanumeric characters preventing MySQL access)
 = Fixed a bug where the /skillreset command was broken
 = Fixed a bug where skill commands displaying .x% instead of 0.x%
 = Fixed a bug Unbreaking enchantments being ignored when using Treefelling and when hit by Armor Impact
 = Fixed a bug where only 1 diamond was needed to fully repair a broken item: Repaired the Repair skill!
 = Fixed a bug where a infinite loop of errors caused by mySQL database could cause the server to crash
 = Fixed a bug where PartyChangeEvent was fired even when a player isn't able to change parties
 = Fixed a bug which caused advanced.yml not to work for Swords
 = Fixed a bug which caused advanced.yml not to respect every MaxChance node
 = Fixed a bug where GreenThumb_StageChange wasn't read from advanced.yml
 = Fixed a bug where Repair would remove enchantments but the glow effect remained
 = Fixed a bug where dropped items did not retain custom NBT data
 = Fixed a bug which caused a potentially infinite recursion in a btree structure
 = Fixed a NPE with custom blocks
 = Fixed a bug with Blast Mining never dropping debris blocks
 = Fixed a bug with Blast Mining incorrectly handling reduced TNT damage
 = Fixed a bug with conflicting fishing enchantments
 = Fixed a bug where triple drops wouldn't happen
 = Fixed a bug which caused fishing to ignore max/min levels in treasures.yml
 = Fixed a bug where treefeller affected player-placed blocks
 = Fixed bug where Skull Splitter would be applied twice.
 ! GJ stopped being a lazy slacker and got stuff done
 ! Nossr50 actually committed something
 ! Changed code that uses SpoutPlugin to make it compatible with the latest version
 ! Reimplemented skill level and power level caps.
 ! Moved Arcane Forging and Fishing setting from config.yml to advanced.yml
 ! Overall SQL query improvements
 ! Reduced number of SQL queries for mcTop command from 11 to 1, speeding it up immensely
 ! Changed FFS Leaderboards to hold information in memory rather than doing IO work (optimizations)
 ! Improved chunk conversion (less errors)
 ! Changed Fishing Treasure Hunter, chance has increased and now actually is level dependent
 ! Indexed most used mySQL columns for faster queries
 - Removed dead code relating to null profiles
 - Removed unused imports
 - Removed ChunkletUnloader and dependents, since they are no longer necessary.

Version 1.3.12
 + Added Craftbukkit 1.4.5 compatibility
 + Added the new 1.3.2 items, xp and double drops for Cocoa beans & Emeralds, EnderChest to the list of blocks that shouldn't trigger abilities
 + Added new items from Minecraft 1.4 to Herbalism (potatoes & carrots)
 + Added new configuration file for advanced users.
 + Added new permission nodes to greenthumb for the 1.4 items
 + Added new mobs from Minecraft 1.4 checks for every ability
 + Added new active ability for Repair: Salvage
 + Added options to 'config.yml' configure shake chance
 + Added the option to negate experience earned for Herbalism while in a minecart to prevent afk leveling
 + Added Green thumb now converts cobble walls to mossy cobble walls
 + Added beacons and anvils to list of blocks that don't trigger abilities
 + Added a configuration option to disable experience gains when in a minecraft for Acrobatics and Herbalism, to prevent AFK leveling
 + Added a new passive ability for Fishing, Fishermans diet. Increases hunger restored from fish
 + Added a feature to display all active perks on login
 ! Changed Fishing, Shake drops changed from guaranteed to based upon fishing level and perks
 ! Changed Woodcutting, the amount of experience earned when using Tree Feller on jungle trees has increased
 ! Changed Herbalism double drop rates for melons and netherwart
 ! Changed filesystem usage, it's reduced a lot. Should help reduce lag on larger servers
 ! Changed database connection handling. Support for aggressive connection timeouts, with exponential backoff for multiple failures
 ! Changed Cobblestone walls are now mossy-able with Greenthumb
 ! Changed the skull drop rates of the shake ability to 3%
 = Fixed a NPE when Citizens perform certain tasks
 = Fixed a NPE with Woodcutting, excessive null chunk before earning Woodcutting experience
 = Fixed a NPE related to skill cooldowns
 = Fixed a NPE when a players profile was null
 = Fixed a NPE involving certain explosions
 = Fixed a dupe bug when for players who were using a 'nuker' client
 = Fixed a dupe bug where pistons were used to dupe ores
 = Fixed a dupe bug with Salvage when players were in Creative mode
 = Fixed a bug where the player was displayed an incorrect cooldown time
 = Fixed a bug where players could earn experience when they were dealing 0 damage
 = Fixed a bug where players could get double drops from mossified Cobblestone
 = Fixed a bug where Herablism magically converted potatoes to carrots
 = Fixed a bug where you couldn't modify the stats of offline players
 = Fixed a bug where treefeller didn't work properly on tree's with side-way logs
 = Fixed a bug where the Arcane forging downgrade chance should've been 0, but actually wasn't
 = Fixed a bug where Fishing would sometimes give items with empty enchantments
 = Fixed a bug where the lucky perk for Fishing was actually an unlucky perk
 - Removed nothing

Version 1.3.11
 ! Changed axes to start with 1 durability damage instead of 5, gain 1 durability damage every 50 levels instead of 30, and only have a 25% chance on hit to damage armor (per armor piece)
 + Added compatibility with bow-wielding NPCs from Citizens/NPC mods
 + Added compatibility for pvp-prevention plugins for Serrated Strikes
 = Fixed bug where mcMMO could throw NPE errors if trees cut down were from a custom mod and had an id of 17
 = Fixed dupe bug where mcMMO would ignore other block-protection plugins for various abilities
 = Fixed NPE with hardcore mode's vampirism
 
Version 1.3.10
 + Added 1.3.1 compatibility
 + Added permission node for Iron Grip ability (mcmmo.ability.unarmed.irongrip)
 + Added ability for custom blocks to drop a range of items.
 + Added Ability API functions
 + Added 50% & 150% XP boost perks
 + Added "lucky" perk for donors
 = Fixed /inspect not working on offline players
 = Fixed custom blocks, tools and armors not loading properly
 = Fixed duplication bug with sticky pistons
 = Fixed "GenericLabel belonging to mcMMO..." message
 = Fixed menu exit button not working
 = Fixed Repair enchant downgrade not working
 = Fixed NPE caused by Spout players after a /reload
 = Fixed ConcurrentModificationException on world unload
 = Fixed players never being removed from memory (memory leak)
 = Fixed admin chat being seen by everyone
 = Fixed issue with UTFDataFormatException occurring on occasion when trying to load Chunklets
 = Fixed ArrayIndexOutOfBounds error caused when trying to use /xplock after logging in but before gaining XP
 = Fixed custom tools not properly respecting the Ability_Enabled flag.
 = Fixed "lower tool" messages still being displayed even when ability messages are disabled.
 = Fixed custom blocks not dropping the proper item with Super Breaker when Silk Touch is used
 = Fixed custom woodcutting blocks throwing errors.
 = Fixed possible ClassCastException from catching something other than a mob when using the Shake Mob skill
 ! Changed the format by which Chunklets are stored to be much smaller, and much faster to load
 ! Optimized how player placed blocks are tracked

Version 1.3.09
 + Added compatibility with AntiCheat (Which I highly recommend to prevent cheating)
 + Added several permission nodes to give individual users special perks (Double/Triple/Quadruple XP)
 + Added reduced cooldown permission nodes as special perks (1/4, 1/3, 1/2 cooldown)
 + Added increased activation time permissions nodes as special perks (+4, +8, and +12 seconds)
 + Added API for plugins to add custom tools directly via Spout - repair / abilities do not work ATM
 + Added offline party members to the list displayed by /party
 + Added possibility to kick offline members from parties
 = Fixed bug that would cause a NPE for players that had no parties
 = Fixed Vampirism not notifying the correct amount of stolen levels
 = Fixed bug with Acrobatics not saving you from deadly falls
 = Fixed /mcremove being applied only after a reload
 = Fixed Archery PVE disablement not working properly
 = Fixed possible NPE when a projectile is shot by a dispenser or doesn't have any shooter
 = Fixed issue with NoCheatPlus and Serrated Strikes / Skull Splitter (fight.noswing)
 = Fixed tiny memory leak concerning Archery
 = Fixed bug where you could receive Archery XP from Potions
 = Fixed bug where Chunklets for the < 64 y coordinates would not be properly loaded
 = Fixed exploit with block duplication via piston pushing
 = Fixed bug with falling sand/gravel not being tracked
 = Fixed bug with Tree Feller not working with custom axes
 = Fixed bug with locale strings when trying to teleport to a non-existent player
 = Fixed bug with Tree Feller changing durability before checking for axe splintering
 = Fixed bug with Repair Mastery permission due to typo
 = Fixed bug with repairing items that use metadata
 = Fixed bug with Chunklets not being reloaded on /reload
 = Fixed possible NPE when falling with no item in hand
 ! API methods can now only be used in a static way
 ! Arrows shot from a bow having the Infinity enchantment can no longer be retrieved
 ! Arrows that aren't shot by an entity are now able to be dodged (currently only from dispensers)
 ! Changed Spout settings to be in their own config file (spout.yml)
 ! Changed file format for parties (parties.yml), previous files are no longer used
 ! Changed mcMMO to inform on corrupt Chunklets and make new ones

Version 1.3.08
 + Added more notifications about Vampirism and Hardcore mode on player death
 + Added information about Hardcore mode when joining a server running Hardcore mode
 + Added new hidden.yml inside the jar for very sensitive config options for advanced users
 + Added option to disable Chunklets for servers which do not have doubledrops and do not care about xp farming
 + Added new "Max_Seconds" setting in config.yml to limit the max time of abilities
 + Added new repair configs to allow customization of the repair skill
 + Added message to inform users about hardcore mode on login
 = Fixed exploit where you could gain tons of Acrobatics XP from spamming Ender Pearls
 = Fixed normal pistons marking a block as user-placed on retract if it wasn't a sticky piston (thanks turt2live!)
 = Fixed handling of the Unbreaking enchantment so that tools are actually damaged as they should now
 = Fixed hurting pet cats with serrated strikes
 ! Changed Hardcore Vampirism to require the victim to have at least half the skill level of the killer in order for vampirism to proc (this is to avoid exploitation)
 ! Changed Hardcore Vampirism to steal a minimum of 1 skill level from a player no matter the percentage
 ! Changed Hardcore & Vampirism to not be executed if percentages were set to zero or below
 ! Changed Vampirism to actually remove stats from the victim
 ! Changed Vampirism to inform the victim of their stat loss
 ! Changed Mining to allow Silk Touch to work again since the dupe exploit has been fixed.
 ! Changed Metrics to also report if the server uses plugin profiling
 - Removed level and item settings from Repair skill in config.yml

Version 1.3.07
 + Added ability to gain XP from custom blocks. Enable custom blocks in the config file, then enter the data in the blocks.yml file.
 + Added ability to gain XP with custom tools. Enable custom tools in the config file, then enter the data in the tools.yml file.
 + Added ability to repair custom tools. Enable custom tools in the config file, then enter the data in the tools.yml file.
 + Added ability to repair custom armor. Enable custom armor in the config file, then enter the data in the armor.yml file.
 + Added functionality which makes a new folder in all world files "mcmmo_data" to store player placed block information in
 + Added new configurable Hardcore mode functionality to mcMMO
 + Added new configurable Vampirism PVP stat leech for Hardcore mode
 + Added new bypass permission node for the negative penalties of Hardcore mode 'mcmmo.bypass.hardcoremode'
 + Added configurable level curve multiplier which allows for tweaking the steepness of the XP needed to level formula
 + Added a permission node for Archery bonus damage
 + Added a permission node for Greater Impact ability
 + Added permission nodes for Treasure & Magic Hunter for Fishing
 + Added a permission node for Farmer's Diet
 + Added config options for enabling/disabling specific double drops
 + Added automatic zip backup of flatfile database & config files
 + Added config options to enable/disable specific skills for PVP & PVE
 = Fixed bug where Tree Feller was looking at the wrong blocks for determining how much to take down.
 = Fixed bug where Green Terra consumed seeds even on Mossy Stone Brick
 = Fixed bug where the client didn't reflect the Stone Brick to Mossy Stone Brick change
 = Fixed bug where an arrow could bounce off entities on daze proc
 = Fixed bug where a player could gain Acrobatics experience while riding a cart
 = Fixed /party not working properly with 2 arguments
 = Fixed /party not showing properly the member list
 = Fixed /ability not checking the right permission
 = Fixed rare NPE on /party command
 = Fixed Arrow Retrieval dropping only one arrow
 = Fixed /p and /a incompatibilities with bChatManager
 = Fixed Iron Grip working reversely
 = Fixed NPE when user clicked the HUD button with Spout
 = Fixed bug where the permission node for Impact didn't work
 = Fixed some bypass nodes defaulting true for Ops
 = Fixed bug with trying to use Chimera Wing while standing on a half-block
 = Fixed duplication bug when a placed block was mined after a server restart
 = Fixed exploit where shooting yourself with an arrow gave Archery XP
 ! Changed the mcMMO motd to link to the new website rather than the wiki
 ! Changed bleeding ticks damage to 1 from 2
 ! Changed Mining to ignore blocks when the pick is enchanted with Silk Touch
 ! Changed Super Breaker to be non-functional when used with a Silk Touch enchanted pick
 ! Changed MySQL to save player information 50ms apart from each other to reduce the load on the MySQL server
 ! Changed the permission node for Blast Mining detonation to mcmmo.ability.blastmining.detonate (was mcmmo.skills.blastmining) for the sake of consistency
 ! Changed skill commands to only display what you have permissions for
 ! Changed mcMMO to use a new storage system for player placed blocks
 - Removed some unused permission nodes
 - Removed a few config options in favor of permissions nodes (Hunger Bonus, Armor/Tool Repair, Instant Wheat Regrowth)
 - Removed level requirement for repairing string tools from the config file

Version 1.3.06
 + Added Iron Golem XP for aggressive golems
 + Added permissions check to skill functions
 + Added API functions for obtaining offline profiles & profiles via player names
 + Added API functions for admin & party chat
 + Added Iron Grip skill to Unarmed which gives players an chance to keep from being disarmed.
 + Added some new languages to the locale files.
 = Fixed Green Thumb consuming 2 seeds instead of 1
 = Fixed exploit where you could teleport to yourself with PTP to prevent things like fall damage
 = Fixed NPE error with Metrics on startup
 = Fixed bug where Herbalism required double drops permission to give XP
 = Fixed bug where {0} would be displayed in front of your power level in mcstats
 = Fixed mmoupdate not being useable from console
 = Fixed bug with repairing wooden tools
 = Fixed bug with Nether Wart not awarding XP
 = Fixed bug with fishing treasures when treasures list is empty
 = Fixed bug with only getting one level when there was enough XP for multiple levels.
 = Fixed bugs with the way /mctop displayed
 = Fixed issues with custom characters & locale files.
 = Fixed double explosion for Blast Mining
 = Fixed Blast Mining not giving triple drops when it should
 ! Changed Bleeding to now stack to a finite number on Monsters and will wear off eventually
 ! Changed how we handled the config file to prevent any bugs when returning values
 ! Changed locale files to use a new naming scheme. This breaks ALL old locale files. If you want to assist with re-translating anything, go to getlocalization.com/mcMMO
 ! Changed /mcremove to check for users in the MySQL DB before sending queries to remove them
 ! Changed how the tree feller threshold worked for the better
 ! Changed /mcremove to no longer kick players when they are removed from database
 ! Changed /mcremove to work on offline users for FlatFile
 ! Changed PlayerProfile constructor to always take a boolean
 ! Changed getPlayerProfile function to work for online & offline users
 ! Changed Archery's Daze to deal 4 DMG on proc (2 Hearts)
 ! Changed /addlevel command to work for offline users
 ! Changed party & admin chat handling to be nicer to developers
 ! Changed /mcrefresh to work from console
 ! Changed /mcrefresh to work for offline players
 ! Changed UpdateXPBar function to hopefully avoid errors
 ! Changed /party to show offline party members
 ! Changed Blast Mining requirements, now asks for the player to be crouching

Version 1.3.05
 + Added Skill Shot to Archery which increases damage dealt by 10% every 50 skill levels (caps at 200%)
 + Added ExperienceAPI and PartyAPI classes for developer use
 + Added ability to cap overall power level
 + Added showing powerlevel below a persons name if you run Spout (optional)
 = Fixed errors when Spout would disable itself after start-up
 = Fixed XP bar not updating when XP was gained
 = Fixed bug with repairing wooden tools
 = Fixed bug where spawned wolves only had 8 health.
 = Fixed bug where rare Treasures from Excavation were dropping too often
 = Fixed bug where Skull Splitter & Serrated Strikes could be used without permissions.
 = Fixed bug where API functions were set to static
 = Fixed bug where mmoedit threw errors when modifying an offline user
 = Fixed dupe exploit with Blast Mining
 ! Changed Tree Feller to account for ability durability loss but not leaves.
 ! Changed bypass node for Arcane Forging to not default to true for OPs
 - Removed Ignition from Archery
 - Removed McMMOPlayerRepairEvent - was basically a duplicate of McMMOPlayerRepairCheck but couldn't be cancelled.

Version 1.3.04
 + Added McMMOPlayerRepairEvent for API usage - fires after completion of a repair.
 + Added McMMOPlayerRepairCheckEvent for API usage - fires before repair process begins, can be cancelled.
 + Added ability to get skill level from McMMOPlayerExperience events
 + Added McMMOPartyTeleportEvent for API usage - fires before a successful teleportation would occur.
 + Added McMMOPartyChangeEvent for API usage - fires whenever a player joins or leaves a party
 = Fixed Shake ability dropping bonemeal instead of ink for squids.
 = Fixed Green Terra & Super Breaker awarding 4x drops at high levels.
 = Fixed summoned ocelots never changing skins.
 = Fixed bug with Disarm not working
 = Fixed some API functions not being visible
 = Fixed bug where /ptp worked on dead party members
 ! Changed MySQL to reload all player information on reconnection
 ! Changed event package structure - be sure to update these if you're using the API in your plugin

Version 1.3.03
 + Added Ocelots to Taming XP tables
 + Added ability to summon Ocelots with Call of the Wild
 + Added offline user functionality to mmoedit
 + Added bookshelves to list of blocks that don't trigger abilities.
 + Added 'mcmmo.repair.arcanebypass' permission node to bypass Arcane Repair and keep your enchantments
 + Added config option to disable Herbalism's instant wheat replanting
 + Added LOTS of new permissions nodes. *CHECK PLUGIN.YML FOR UPDATES*
 + Added Italian locale file - thanks Luxius96!
 + Added ability to inspect Ocelots with Beast Lore
 + Added console functionality to mctop
 = Fixed Green Terra not awarding Triple Drops
 = Fixed ClassCastException from Taming preventDamage checks
 = Fixed issue with Blast Mining not seeing TNT for detonation due to snow
 = Fixed issue with block interaction returning NPEs
 = Fixed issue where every block broken had a mining check applied
 = Fixed issue where every block broken had a herbalism check applied
 = Fixed issue where blocks weren't being removed from the watchlist
 = Fixed exploit where you could use /ptp to teleport to anyone
 = Fixed bug where Green Terra didn't work on Stone Brick
 = Fixed bug where Tree Feller could be used without permissions
 = Fixed exploit where falling sand & gravel weren't tracked
 = Fixed exploit where Acrobatics could be leveled via Dodge on party members.
 = Fixed exploit where you could gain combat XP on animals summoned by Call of the Wild
 ! Changed mcMMO to save profiles only when the profile is about to be discarded rather than on player quit
 ! Changed MySQL to try to reconnect every 60 seconds rather than infinitely which caused server hangs
 ! Changed mcMMO to be better about saving player information on server shutdown
 ! Changed PTP to prevent teleporting if you've been hurt in the last 30 seconds (configurable)
 ! Changed Chimera Wing failure check to use the maxWorldHeight.
 ! Changed inspect failed message to say inspect rather than whois
 ! Changed Call of the Wild to activate on left-click rather than right-click
 ! Changed Blast Mining to track based on Entity ID vs. Location
 ! Changed mmoedit to save a profile when used (this will make mctop update)
 ! Changed a few Runnable tasks to have their own classes
 ! Changed parties so that a player will leave their existing party if they enter a world where they don't have party permissions.
 ! Changed Call of the Wild to summon animals already tamed.
 ! Changed mob spawner tracking to use new Metadata API
 ! Changed block watch list to use new Metadata API
 ! Changed around a few config options, including the ones for mySQL. *YOU NEED TO REDO YOUR CONFIG FILE*
 - Removed 'true/false' debug message from Inspect command

Version 1.3.02
 + Added in game guides for Mining, Excavation, and Acrobatics. Simply type /skillname ? to access them
 ! Changed Tree Feller to hand out 1/4 of normal XP for each JUNGLE LOG block it fells
 ! Changed Tree Feller to only fell trees if you have enough durability
 ! Changed Tree Feller to cause injury if your axe splinters from a failed Tree Feller attempt
 ! Changed invincibility checks in EntityDamage listeners to accommodate for vanilla MC behaviour
 ! Changed Ignition to add fire ticks rather than replacing them.
 ! Changed Axes critical to have a max critical rate of 37.5% down from 75%
 = Fixed bug where Taming defensive checks got called twice
 = Fixed Shake not working correctly
 = Fixed bug with Axes command displaying wrong Greater Impact bonus damage
 = Fixed bug where Impact didn't apply bonus damage
 = Fixed Impact proccing multiple times in a row
 = Fixed bug where PVE skills didn't level

Version 1.3.01
 = Fixed bug where Tree Feller had no cooldown
 = Fixed bug with activating Skull Splitter after using Tree Feller
 
Version 1.3.00
 + Added ability to customize drops for Excavation skill (treasures.yml)
 + Added ability to customize drops for Fishing skill (treasures.yml)
 + Added messages to nearby players when your abilities wear off
 + Added jungle trees to Woodcutting XP tables
 + Added player notification for when they stop Bleeding
 + Added configuration option to control mcMMO reporting damage events
 + Added hunger regain bonuses to Herbalism skill
 + Added Blast Mining subskills to Mining
 + Added Fast Food Service subskill to Taming
 + Added size limit to Tree Feller in config as Tree Feller Threshold
 + Added /inspect (works on offline players)
 + Added /addlevels commands
 + Added /mcremove command which lets you remove users from MySQL or FlatFile
 + Added config values for XP multipliers for different hostile mobs
 + Added 'mcmmo.commands.inspect' permission node for the new /inspect command
 + Added Impact & Greater Impact subskills to Axes
 + Re-added mcMMO reporting damage events
 = Fixed bug with updating MySQL tables to include fishing on servers using custom table prefixes
 = Fixed bug where Disarm didn't work at all ever
 = Fixed bug where Swords command showed Bleed Length twice instead of Bleed Chance
 = Fixed bug where Tree Feller wasn't checking for Tree Feller permission
 = Fixed bug where Leaf Blower required Tree Feller permissions rather than Woodcutting permissions
 = Fixed Leaf Blower preventing the use of shears to collect leaves
 = Fixed Green Thumb & Green Terra not consuming or requiring seeds to replant Wheat
 = Fixed Super Breaker & Giga Drill Breaker failing to damage tools
 = Fixed Tree Feller not giving proper XP for different kinds of trees
 = Fixed Skill Abilities conflicting with NoCheat
 = Fixed memory leak with mob spawner tracking
 = Fixed /mcability not respecting permissions
 = Prettied up new config files
 = Various skill function optimizations
 ! Changed how mcMMO calculates distance between two points (optimizations)
 ! Changed how mcMMO handles MySQL connections (optimizations)
 ! Changed the description /mcmmo provides to be more up to date and relevant
 ! Changed mcMMO user information to be stored for 2 minutes after log out to reduce lag on rejoins
 ! Changed Food+ to be named Farmer's Diet in Herbalism
 ! Changed default values of Woodcutting XP tables
 ! Changed 'Pine' to be renamed 'Oak' in Woodcutting XP tables
 ! Changed the name of Unarmed Apprentice/Mastery to Iron Arm Style
 ! Changed Axes to gain bonus damage every 50 skill levels
 ! Changed Unarmed to start with a +3 DMG (1 Heart = 2 DMG) bonus from Iron Arm Style to make leveling it more viable
 ! Changed Unarmed to gain bonus damage every 50 skill levels
 ! Changed Unarmed to gain more bonus damage total than before
 ! Changed Unarmed to have a max disarm chance of 33.3% rather than 25%
 ! Changed Tree Feller to take down entire trees
 ! Changed mob spawn tracking to use Unique Entity ID instead of Entity Object
 ! Changed stats command name to mcstats for better plugin compatibility
 ! Changed god mode to turn off if player enters world where he does not have mcgod permission
 ! Changed Taming to also gain XP from animal taming
 ! Changed Swords Bleeding effect to never kill
 ! Changed Bleeding to never go beyond 10 ticks
 ! Changed to use Bukkit's built-in ignoreCancelledEvents system
 ! Changed chat logging for /p & /a
 ! Changed Tree Feller to use per-use ArrayList
 - Removed /mcstats console functionality
 - Removed /whois command (replaced with /inspect which has similar functionality)
 - Removed Master/Apprentice chat notifications to reduce spam
 - Removed MySpawn system (You can still use Chimaera Wings) due to being outdated and unwanted
 - Removed duplicate settings in config.yml
 - Removed unused settings from config.yml (HP Regen)
 - Removed Nether Brick from Mining XP Tables
 - Removed Stone Brick from Mining XP Tables
 
Version 1.2.12
 - Fixed issue that caused terrible MySQL performance and negative XP on levelup (Issue #134)
 - Fixed addxp command taking xprate and skill modifiers into account
 - Added anonymous usage statistics (you can opt out in plugins/PluginMetrics/config.yml)
 - Modified onEntityDamage priority to have better compatibility with other plugins (Factions, WorldGuard, etc...)
 - Fixed /mcgod & /mmoedit permissions defaulting to true
 - Fixed Fishing not working or handing out XP
 - Fixed error with Skull Splitter / Serrated Strikes that caused server instability and log spam
 - Fixed config.yml not having values for End Stone & other new mining blocks
 - Fixed Green Thumb/Green Terra not correctly planting wheat (Issue #133)

Version 1.2.11
 - Removed legacy Permission & PEX dependency. (PEX still works fine with mcMMO)
 - Made Smooth Brick to Mossy Brick and Dirt to Grass for green thumb configurable (Issue #120)
 - Added MagmaCube to XP tables
 - Made optimizations to Skull Splitter/Serrated Strikes
 - Made it so players take damage if they try to log out with Serrated Strikes stacked onto them (Issue #131)
 - Changed mcMMO to save data periodically to optimize performance with FlatFile & MySQL (Issue #138)
 - Added a configurable save interval for the new save system
 - Fixed a bug with the odds calculations for Serrated Strikes
 - Fixed several commands not working from console (mmoedit, etc..) (Issue #150)
 - Added a success message when executing xprate from console

Version 1.2.10
 - Fixed issue with receiving Woodcutting XP for all blocks broken (Issue #103)
 - Fixed issue with Spout images & sounds not working (Issue #93)
 - Fixed typo with repairing Leather Armor & Bows
 - Fixed issue with Silk Touch & Double/Triple drops not working properly
 - Fixed conflict with NoCheat plugin & Super Breaker/Giga Drill Breaker/Berserk/Leaf Blower (Issue #104)
 - Fixed counter-attacking non-LivingEntity (Issue #100 & Issue #107)
 - Fixed various bugs with Leaf Blower
 - Added Monitor & ignoreCancelledEvents to onBlockPlace
 - Made Anvil ID configurable

Version 1.2.09
 - Fixed issue with Repair Mastery (Issue #47)
 - Made Arcane Forging fully configurable (Pull Request #52)
 - Made Fishing configurable (Pull Request #60)
 - Changed timer to be a bit more efficient (Issue #19)
 - Changed to fire EntityDamageEvents for all damage done by mcMMO
 - New custom event for developers McMMOPlayerLevelUpEvent
 - New custom event for developers McMMOItemSpawnEvent
 - Changed LoadProperties from the old Configuration to FileConfiguration
 - Removed aliasing from config.yml
 - Fixed mining procs from Super Break & Silk Touch
 - Unused smelt property removed
 - Minor optimizations
 - Fix for setting properly block damage values
 - Initial skill level capping added
 - Initial command alias framework added
 - Fixed abilities not handling Unbreaking items
 - Fix for treefeller glitch
 - Super secret anniversary easter egg!

Version 1.2.08
 - Changed Bukkit events to new event system
 - Changed aliasing to send both the mcmmo command and the command used.
 - Changes in combat exp (Pull Request #49)
 - Repair for bows & leather armor (Pull Request #46)
 - Fixed missing images (Pull Request #45)
 - POM Changes for dependencies (Pull Request #36)
 - Fishing & Repair fixes (Pull Request #31)
 - Fixed CraftOfflinePlayer issue (Issue #212) errors for offline wolf owners
 - Pull in commit from @NuclearW for issue from previous commit

Version 1.2.07
Fixed mctop not working at all (whoops!)
Fixed problem with multithreading in mcMMO causing errors
Fixed bug with Repair where it would remove the enchantments if you could not even repair the item
The command mmoupdate now runs in its own thread to ease the burden on the server

Version 1.2.06
German translation has been updated
Fixed fishing not being applied to MySQL DB when converting from Flat File -> MySQL
Fixed mctop not taking Fishing into account some of the time
Fixed bug where Taming would try to grab the name of offline players
Fixed bug where Fishing would try to add an enchantment level not normally possible
Fixed another bug with mmoedit and Fishing
Added option to only allow tools to ready when you are sneaking, this is off by default
Added Brewing Stand & Enchanters table to the list of blocks that won't cause you to ready your tool on right click

Version 1.2.05
Fixed my fix of not being able to place blocks near/on Anvils
Fixed resources in inventory not correctly updating after Repair

Version 1.2.04
Fixed bug where you could not place blocks near/on the Anvil

Version 1.2.03
skills2 and experience2 will be removed from MySQL DB automagically when this version first runs
Fishing is now stored in skills and experience tables on the MySQL DB as it should have been
Fishing will now save properly for MySQL
Fishing will now work properly with mctop for those using MySQL
Fixed problems with mmoedit and fishing

Version 1.2.02
Added measures to prevent easy xp from hacks that cause a ridiculous amount of clicks per second
Fixed bug where Call Of The Wild used only 1 bone to summon
Reduced Endermen XP from 3x to 2x
The number of bonus fish caught from fishing has been reduced
Fishing XP reduced from 1500 to 800
Fishing XP is now configurable in the config file

Version 1.2.01
Added a setting to turn off abilities completely from config
Added a setting to just turn off ability messages from config
Fixed the bug with sword repair
Fixed mcMMO not working properly with Spout
Added Fishing XP icon to Normal/Retro HUDs for Spout
Added icons to Spout notifications for leveling Fishing
Added Fishing Retro XP bar color customization to config file
The number of bones required to use Call of The Wild is now configurable
Reduced the XP animals would give from 1.5x to 1x
Removed current durability value message from Repairing
Fixed bug where Arcane Forging failed to display messages
Fixed bug where Arcane Forging tries to downgrade level 1 enchants
Fixed bug where Arcane Forging always kept enchantments if you had under 100 Repair skill

Version 1.2.00
Added Fishing Skill
Added Call Of The Wild to Taming
Added Arcane Forging to Repair
Added new mobs to XP tables
Added Master/Apprentice system to the Party system
Animals now give xp to combat skills (those poor sheep ;_;)
Removed unnecessary sorcery permissions from plugin.yml

Version 1.1.17
XP gained in combat is now softcapped by the remaining health of the entity you are damaging, preventing many exploits.
Players in Creative mode no longer gain XP
Compiled against latest Spout & CraftBukkit
Added World PVP check to Ignition, should no longer ignore PVP settings
Enemies should no longer grant XP when hit during their death
Fixed an exploit that led to unlimited ability use
Possibly fixed a bug where the same player would be listed multiple times in mctop
Added author and description to plugin.yml

/mmoedit and /addxp are useable from the console now
Swearword's statistics tracking removed (He stopped the service, so its gone now.. On a positive note, I did find out 1000-1500 servers installed mcMMO a day)

Version 1.1.16
Added Melons to Herbalism xp tables
Endermen added to Combat skill xp tables
Silverfish added to Combat skill xp tables
CaveSpider added to Combat skill xp tables

Version 1.1.15
Smooth Brick added to Green Terra
Green thumb can be used to spread moss to Smooth Brick now
Implemented a ghetto fix for the sword durability bug (real fix sometime soon)
Added Spain Spanish localization (es_es)

Version 1.1.14
[1.8] Removed the Archery fire rate limiter as its no longer necesarry due to changes in game mechanics
[1.8] Removed the bonus damage from Archery (I'll rework this skill soon)
[1.8] Removed the food bonuses to healing Herbalism provided due to the change of eating in game mechanics
[1.8] Swords no longer parry, no need to compete with in game mechanics
[1.8] mcMMO no longer has an HP Regen system, no need to compete with in game mechanics
[SPOUT] mcMMO now transfers files between [MC Server] -> [Client] rather than [Webserver] -> [Client]
[SPOUT] Temporarily disabled the PartyHUD due to some performance issues
[SPOUT/CONFIG] mcMMO now allows for disabling of the party HUD with the node Spout.Party.HUD.Enabled
[BUG] Fixed a few problems with readying abilities for Woodcutting/Axes
[MYSQL] Improvements have been made to the performance of MySQL thanks to krinsdeath
[CONFIG] Spout.Party.HP tree removed, replaced with Spout.Party.HUD
[CONFIG] Added an option for Excavation to require use of a shovel, on by default
[COMPATIBILITY] Changed the listener priority for OnEntityDamage from High to Monitor (Should make mcMMO compatible with Worldguards pvp regions among other things)
[COMPATIBILITY] Made party/admin chat modes more compatible with chat plugins (vChat)
[API] Added addXpOverride for modders, this will ignore skill modifiers
[SPOUT] The option to change the weburl of mcMMO Images/Sounds has been removed, if you want to customize mcMMO images/sounds you can open mcMMO.jar and replace them there
[LOCALE] Portuguese Brazil locale added (Code: pt_br)
[MISC] Added some experimental usage tracking, you can opt out of this in /plugins/stats/config.yml (Once its generated, may require 2 restarts)

Version 1.1.13
Pets are removed from party bars

Version 1.1.12
mcMMO now downloads files when you join the server to provide the best experience
mcMMO now uses a brand new Party HUD by Rycochet (from his mmoParty plugin)
Fixed the xpbar and xpicon settings in config to work properly
Fixed infinite HP exploit with Herbalism
Fixed bug where herbalism would heal out of the players normal health range
Fixed bug where entering ':' into your party name caused stat loss among other things
Fixed issue with block break listener priority

Version 1.1.11
mcMMO now properly cancels its Async taks when disabled
Fixed newly generated configs using 2 instead of 1 for skill multipliers

Version 1.1.10
Added default hud setting to config
Fixed bug where newly generated configs used old xp gain numbers

Version 1.1.09
Fixed mcMMO to run fine without Spout :)

Version 1.1.08
Fixed repair being 10x slower to level than normal

Version 1.1.07
Fixed the default HUD being set to RETRO instead of STANDARD

Version 1.1.06
mcMMO menu implemented! Default is 'M', change this in config
Retro HUD implemented!
Retro XP fill color is completely customizable on a per skill basis
New levelup sound thanks to @Rustydaggers !
With the help of Randomage the XP Formulas have been vastly changed for flexibility
Global modifiers and skill modifiers now support decimals
Global formula modifier dropped from config
GigaDrillBreaker/Berserk doesn't drop clay blocks anymore
Fixed bug where Herbalism didn't heal more for bread/stew when right clicking a block
Fixed bug where Wheat did not use the values form the config file
Fixed bug where Archery gave xp for inflicting self injury
Watch added to clay loot tables and maps remove from clay loot tables

Version 1.1.05
Maps dropped from excavation are created correctly, and represent the area they are found in
Fixed an exploit with clay and excavation
Fixed a NPE with locking xp bars
Fixed the !AdeptDiamond! localization error when repairing diamond with a skill below 50

Version 1.1.04
Removed URL settings for XPBAR/XPICON/HPBAR
Added single URL setting for mcMMO
Changed default host from Dropbox to Rycochet's webserver (with apparently unlimited bandwidth!, thanks Rycochet)
Fixed Repair noise not getting played
Fixed a small memory leak with party health bars

Version 1.1.03
Fixed a few images being hard-coded still rather than configurable

Version 1.1.02
Fixed bug where toggle for xpicon didn't work
Fixed bug where Excavation gave gravel drops to grass
Excavation now uses more enums

Version 1.1.01
Fixed toggles for hpbar/xpbar not working

Version 1.1.0
Brand new XP Bars, Health bars, and Skill Icons designed by BrandonXP
Added /xplock <skillname> to lock the xp bar to a skill
Repairing metal now has a sound effect
Shears added to Repair
MySpawn now works correctly when you are in the nether
MySpawn message when you right click a bed is now squelched
Intervals at which players renegerate hp have doubled in length (making it take 100% longer to regenerate than before)
Rewrote many variables stored per player to be integer instead of long, reducing overall memory usage of mcMMO
Rewrote the Timer mcMMO relies on to instead use the BukkitScheduler for performance
Fixed the party member list of /party
Fixed bug where Swords would counter-attack Projectiles
Removed a debug message when repairing diamond armor
Changed chat to use getDisplayName() instead of getName()
Changed chat priority from lowest to highest
Added Clay to excavation
Added new items to Clay's loot tables
Archery now works with the latest CB

Version 1.0.50
New /xprate command for those with mcmmo.admin permissions!
mcMMO now uses Spout instead of BukkitContrib
BukkitContrib support dropped
XP Formula is now 100+(skill level value * skill modifier * global modifier) thanks to suggestion
Fixed bug where /mmoupdate used the old directory instead of the new one to find the flat file
Fixed bug where Unarmed Mastery damage bonus only did as much as Unarmed Apprentice
Fixed bug where Pumpkins did not give out XP
Coordinates removed from /whois as they didn't really fit
/mcgod and /mmoedit now require permissions to be setup in some shape or form to be used
Lapus renamed to Lapis in config

Version 1.0.49
Updated German locale
Fixed bug where using the party system on a MySQL setup caused errors when writing to non-existent files
Fixed bug where using /accept caused a NPE (hopefully)
Fixed a few missing descriptions for commands

Version 1.0.48
Updated French Translation
Updated German Translation
Updated Polish Translation
Placed Coal Ore and Redstone Ore won't give XP anymore
Fixed unusually high memory usage at startup
Added many features to the party system written by NuclearW

Version 1.0.47
Fixed another BukkitContrib error for servers not running BukkitContrib

Version 1.0.46
Fixed bug preventing Excavation from gaining skill

Version 1.0.45
Corrected /stats showing Repair XP as Level for Repair
Corrected /repair showing Repair XP as Level for Repair
Corrected /whois showing Repair XP as Level for Repair

Version 1.0.44
Fixed my 'fix' of BukkitContrib errors with Tree Feller

Version 1.0.43
Stopped things from being auto-smelt'd

Version 1.0.42
Corrected 2 more errors involving not running BukkitContrib

Version 1.0.41
Fixed errors using Tree Feller if your server wasn't running BukkitContrib (sorry!)
Fixed some more leftover stuff involving the new half-finished mining skill
Fixed excavation's Giga Drill Breaker not working on placed blocks

Version 1.0.40
Fixed errors if your server wasn't running BukkitContrib

Version 1.0.39
mcMMO won't auto-download and auto-run BukkitContrib anymore

Version 1.0.38
Commented code for the half-finished Infernal Pick subskill (Whoops)

Version 1.0.37
The donation message in /mcmmo is now toggle-able
The anvil message now only gets shown the first time you place an anvil (after login)
Reworked /mcmmo (an improvement I would say)
Added /mcmmo text to localization file
Archery fire rate now configurable
Berserk mode stops items from being collected
Taming no longer receives xp from wolves being harmed
Fixed bug where /stats required Tree Feller permission to show Woodcutting skill
Fixed bug where players with mcgod could be harmed by AoE
Fixed bug where modifying a skill also modified the xp to the same amount (when it should be zero)

BukkitContrib Stuff
Added a pop-up when placing an Anvil
Added pop-ups on levelup
Added basic sound effects to various abilities (Berserk, Tree Feller, Super Breaker, Leaf Blower, etc...)

Code Stuff
Added checkXp(SkillType, Player) for plugin devs (use this after modifying XP to check for levels)
Added getPlayerProfile() which returns a PlayerProfile object for plugin devs (You can do almost everything with this object)
100% more enums
Changed how checking skill xp worked to be more efficient

Version 1.0.36
mcMMO now properly supports Bukkit/PEX/Permissions for Permissions
Config.yml will no longer generate Performance Debugging nodes
Registered permission nodes to plugin.yml
Some more changes to Permissions code
Fixed bug where Super Breaker activated where it shouldn't
Fixed bug with enabling/disabling mcgod in config.yml
Fixed bug with Excavation not kicking in until 1 level higher

Version 1.0.35
Added a Toggle for Chimaera Wing in config.yml
Added customization of what item is used for Chimaera Wing in config.yml
Fixed bug with randomly receiving Taming XP
mcmmo.users file moved into /plugins/mcMMO/FlatFileStuff/
Leaderboard files now moved into /plugins/mcMMO/FlatFileStuff/Leaderboards
Locale files now have the prefix locale_ instead of messages_
Locale files are now located inside com/gmail/nossr50/locale/ instead of com/gmail/nossr50/
Updated the code that handles permissions (this may mean 3.1.6 will finally play well!)
Some more source code organization
Fixed warnings for compiler
Removed dependencies on CraftBukkit
Registered commands to OnCommand
Removed performance debugging
Removed some useless settings from the config file

Version 1.0.34
Fixed the PVP setting determining whether or not you would hurt yourself from AoE Abilities
Added Dutch (nl) language support
Super Breaker now gives the correct XP as determined by config.yml
Sand Stone XP is now configurable and no longer shares the 'stone' node
/mining now shows mining values instead of taming values

Version 1.0.33
Fixed the toggle for the Excavation drop 'Cocoa Beans'
Fixed bug where Unarmed users could disarm without being bare handed
Cocoa Beans now have an XP modifier in config.yml
You can now toggle whether or not Mobspawners will give XP (in config.yml)
MySQL version now makes requests to the MySQL server less frequently (should help performance)
Fixed bug with Skull Splitter hitting the user

Version 1.0.32
Added "General.Performance.Print_Reports" node to config.yml to help identify causes of performance issues
Fixed bug of swords users hurting themselves with serrated strikes

Version 1.0.31
Fixed bug of trying to cast Animals to non-animals

Version 1.0.30
Mobs that spawn from spawners no longer give XP (for reals this time)

Version 1.0.29
Mobs that spawn from spawners no longer give XP (again)
Fixed bug where Serrated Strikes did not Bleed additional targets
Identified and solved a potential memory leak in Bleed Simulation
Renamed the Object Config to Misc and rewrote parts of it
Rewrote Party/Admin/God toggles
Added Polish language support (pl)

Version 1.0.28
Actually fixed /stats showing excavation values for swords
Made some improvements to how Bleed Simulation was handled for different entity types
Obsidian now does normal durability damage during Super Breaker

Version 1.0.27
Fixed /stats showing excavation values for swords
Hopefully fixed a wide range of NPE errors
Updated German (de) localization

Version 1.0.26
Fixed accidentally making power levels go above 9,000

Version 1.0.25
Compatible with the latest CB
Beast Lore now functions correctly
Wolves are no longer invincible to players
Changed the look of Beast Lore
Skill info pages now show your stat in that skill (if you have permission)
/stats and /whois has been alphabetized and divided into three categories (Gathering/Combat/Misc)
Abilities will not trigger on Trap Doors

Version 1.0.24
Now compatible with latest RB (928)
Taming now receives XP from your wolves harming foes
Taming is now easier to level
Green Thumb now drops seeds when harvesting Wheat

Version 1.0.23
Modified Bleed Simulation to fix performance problems
Rewrote MySpawn to be more efficient when calculating time left
Rewrote Skills to be more efficient when calculating time left

Version 1.0.22
Added 'Name' nodes to commands for renaming them

Version 1.0.21
Fixed Skull Splitter length in /axes displaying incorrectly
Fire rate limiter now correctly uses the value in the config file
Stone XP now correctly uses the value in the config file
Cobble -> Mossy now correctly uses the value in the config file
Removed setmyspawn from config file as it serves no purpose
All commands now have an 'Enabled' node in the config file that when set to false disables the command completely
Fixed color scheme inconsistency for Mining in /whois results

Version 1.0.20
Fixed Array Index Out of Bounds error

Version 1.0.19
Removed a failsafe for the Timer that is no longer necessary (should improve performance)
Fixed /myspawn not working by rewriting it :3
Fixed exploit where players could break a freshly placed mushroom for XP
MySQL User Passwords can now be blank (Although you really should have a password...)
Fixed a few NPE errors

Version 1.0.18
Fixed MySQL default TablePrefix
Fixed Wheat not being configurable

Version 1.0.17
Brand new YAML Configuration file
Ability to configure XP for all gathering skills in config file
German Language added to mcMMO
French Language added to mcMMO
MySpawn will no longer heal players
/<skillname> commands now also check for their localized names for displaying help
Added many more Strings to localization files
Added more safeguards to MySpawn for NPE
Fixed bug where Tree Feller Radius depended on WoodCutting XP rather than Skill Level
Fixed bug where Readying a Hoe returned a missing localization string
Added some safeguards into Bleed Simulation to prevent possible memory leaks
Performance improvements to storing/calling Skill/XP Values
Plugged a potential memory leak with PlayerProfiles not being removed correctly
Disabled the mob spawner camping anti-exploit in favor of performance

Version 1.0.16
Fixed bug where localization file failed to load
Changed en_US to lowercase
mcMMO now requires locale files to be in lowercase
Fixed a few strings missing from the localization file

Version 1.0.15
Removed leftover code that spammed SQL errors

Version 1.0.14
Added many missed strings into localization
Finnish Localization updated for the new strings
Green Thumb should respect Block Protection plugins now
Fixed Number Format Exception when loading a PlayerProfile

Version 1.0.13
Fixed bug/NPE where stats would not load and therefore 'reset' for players
Fixed NPE involving /ptp
Added "enableMOTD" setting to properties file

Version 1.0.12
Fixed another NPE error
Non-Gathering skills should correctly gain XP if PVP is set to false now
Localization will now support language codes that do not have two parts like "fi"
Fixed bug where Wiki MOTD message would not be loaded from localization file

Version 1.0.11
Fixed bug where players could not gain experience in several skills
Removed PVP flag from mcmmo.properties as its not needed anymore
Fixed a few NPE errors
Mushroom XP reduced from 25 to 15
Fixed an exploit where players who just logged in could be farmed for experience because they were invulnerable

Version 1.0.10
Added Localization/String Customization
Mushroom XP reduced from 40 to 25
Removed "clears inventory" warning in /mcc for /myspawn since this no longer happens

Version 1.0.09
Fixed the NPE that occurs when players gain experience (Sorry!)
Fixed bug where /myspawn & /clearmyspawn would work if MySpawn was disabled in the properties file
Changed strings containing "MMO" to read "mcMMO"
Removed a lot of unused or unnecessary variables from the PlayerProfiles in mcMMO, this should lower the memory footprint
Added getXpToLevel() for modders

Version 1.0.08
Added removeXP() for modders
Fixed bug where stone swords only repaired by 33% instead of 50%
Fixed bug where stone/wooden hoes wouldn't repair
Big overhaul to how skill values and xp values were handled in the code
Modifying the players skill levels now sets the corresponding skill xp to zero
Using Serrated Strikes/Skull Splitter on mobs should no longer harm nearby players when PVP is disabled
Switching to another weapon after firing your bow should no longer trigger procs for that weapon when the arrow hits
Slimes/Ghasts now give XP for combat skills
Added "EnableHpRegeneration" property setting
Added "EnableMySpawn" property setting

Version 1.0.07
Added more repair customization by solarcloud7
Leaderboards ignore players with the respective stat at 0
Reconnecting to MySQL will reload player data
Fixed a NPE with MySQL's Leaderboards
Removed "Loop iteration" debug message from mcMMO

Version 1.0.06
MySQL will attempt to reconnect if the connection is closed
Breaking the bottom block of Cactus/Reeds will award the correct experience and double drops
Added support for Minecraft Statistics
Fixed NPE with /myspawn command

Version 1.0.05
PVP interactions now check for permissions before handing out any experience
Many skill abilities now check for permissions correctly
All interactions with Taming now check for permissions
mcMMO now checks for its pvp flag being true before handling pvp interactions

Version 1.0.04
Fixed bug where players would be informed incorrectly when their cooldowns refreshed
Fixed exploit where players could reconnect to reset their cooldowns
Added new "cooldowns" table to MySQL
Berserk now breaks through snow
Lightning no longer gives Taming XP
Shortened /mcc to fit the screen

Version 1.0.03
Bleed will no longer trigger on friendly wolves
Axes criticals will no longer trigger on friendly wolves

Version 1.0.02
Fixed bug where the Timer would start before everything else was ready
Fixed bug where mcrefresh also required mcability permission node
Fixed bug where Unarmed was not checking for disarm procs
Green Thumb now checks for herbalism permissions
Added "enableGreenThumbCobbleToMossy" to config file, this also changes Green Terra
AoE abilities now harm wolves

Version 1.0.01
Removed debug message when wolves are struck
Fixed issue with reloading mcMMO when MySQL was enabled
Fixed a NPE with MySpawn
Fixed a NPE with removing users from PlayerProfile
Unarmed no longer starts with a damage bonus
Unarmed apprentice DMG bonus changed from 3 to 2

Version 1.0
Players can now repair Stone/Wood tools
Fixed duping bug with WG/Block Protection Plugins
Added Leaf Blower to WoodCutting
Different Trees give different WoodCutting XP
Water changing Gravel to Clay removed
Code Organized/Optimized further
MySQL Support
Taming Skill
Leaderboards
Players won't hand out XP if they died within the last 5 seconds

Version 0.9.29
Fixes critical bug involving water turning anything into clay

Version 0.9.28
Green thumb can now spread grass to dirt using seeds
Adding XP will check for level ups again
Acrobatics won't hand out XP on death anymore
Acrobatics will check plugins for the event being cancelled before handing out XP

Version 0.9.27
Fixed Herbalism not properly receiving Triple Drops from Green Terra
Fixed Herbalism not handing out any XP outside of Green Terra
Fixed Herbalism asking for seeds on things that did not require it

Version 0.9.26
Fixed Green Terra going off without readiness
Fixed Hoe trying to ready when tilling Grass

Version 0.9.25
Fixed issue with anti-exploits and Herbalism
MySpawn works like a hearthstone now, no inv pentality, 1hr cooldown
Added Green Terra Ability to Herbalism
Added Green Thumb ability to Herbalism
Fixed Repair not working for Iron Tools
Fixed bug where Axes Ability checked for Unarmed Ability Permission
Added Cocoa Beans to Excavation XP/Loot Tables, Found in Grass/Dirt
Using Super Breaker on Obsidian significantly damages it compared to other materials
Added Obsidian to Mining XP Table/Super Breaker
Added Pumpkins/Reeds/Cactus to Herbalism XP Tables/Double Drops
Corrected "mcMMMO" to "mcMMO" in MOTD

Version 0.9.24
PLAYER_BED_ENTER removed due to its unusual issues
Added info about the Wiki to the motd
/mcrefresh will reset if you were recently hurt (Chimaera Wing/HP Regen)
Fixed Armor Repair not adding XP
Boosted Repair XP of Armor to match Tools
Repairing Armor won't trigger Super Repair twice anymore
Setting your MySpawn now just requires right clicking a bed (still requires the setmyspawn permission node)

Version 0.9.23
Players will now announce ability usage within a short distance to nearby players
Chimaera Wing now takes the world into account
Acrobatics won't give XP on death, and will fail if you would've died after the damage reduction
Added yet another check to see if a Player is not in the Users system for NPC mod compatibility


Version 0.9.22
Fixed bug where chimaera wing was unusable after being hurt even after the cooldown

Version 0.9.21
/mcrefresh fixed to work properly with the new ability monitoring system
Ability lengths are now based on your skill level directly rather than a tiered system
Chimaera Wings won't trigger on things they shouldn't (Doors, Chests, ETC)
Chimaera Wings will properly tell you how long you have to wait to use it if you've been recently hurt

Version 0.9.20
Fixed Tree Feller not checking if their cooldown was refreshed and always activating
/stats and /whois will now show the powerlevel based on permissions
Shovels will no longer say you've lowered your axe
/myspawn will no longer say your inventory has been cleared if the server settings disable this feature


Version 0.9.19
Fixed Anti-Exploit XP stuff not working

Version 0.9.18
Added failsafe to prevent abilities from going on forever, abilities will check if they should've expired when being used in case the Timer fails
Archery Spam has been nerf'd, you can only fire once per second now (Toggle-able in config file)
Fixed bug when just having the Admin Chat permission wouldn't allow you to see Admin Chat
Fixed bug where Axes ability could be used without permission
Abilities are monitored with Timestamps rather than a Timer monitored tick rate
When players were last hurt is now monitored with Timestamps rather than a Timer monitored tick rate
Made Anti XP-Exploits more Robust
Repair XP is now based on durability restored
Acrobatics rolling will now reduce damage if you go over the damage threshold
Acrobatics rolling damage threshold lowered to 10 from 20
Added Graceful Roll to Acrobatics, hold Shift when falling to do a Graceful Roll
mcMMO now checks for the blockBreak and EntityDamage events being canceled before proceeding
Dodge notification shortened
Dodge won't negate damage completely anymore
Added 3 more functions for plugin authors to call, getPartyName(Player player), inParty(Player player), and getParties()

Version 0.9.17
Players now set their MySpawn by entering a bed, it requires the setmyspawn permission node
/setmyspawn has been removed
Compatible with CB 670
Fixed errors related to Repair
Abilities will no longer trigger from Bed interactions
/unarmed will now tell the player when they will receive unarmed master (if they have apprentice)

Version 0.9.16
Logs placed by the player won't grant XP/Double Drops anymore
Added more functions plugin authors can call
Acrobatics roll has a damage threshold of 20, going above this means a failed Roll


Version 0.9.15
Acrobatics will now behave properly
AoE Abilities ignore wolves (temp fix)
Added "all" parameter to /mmoedit & /addxp
After giving XP to a player it will now check for level ups in skills

Version 0.9.14
mcMMO checks for abilities being active before sending the fake block break event

Version 0.9.13
Fixed excavation ignoring the xpGainMultiplier
Now compatible with CB 600+
Fixed bug where Dodge acted maxed out no matter your skill level

Version 0.9.12
mcMMO now fakes a block break event for abilities to maximize plugin compatibility
/herbalism will return the correct values now
New /addxp command

Version 0.9.11
PVE Combat Skills experience is now based on damage dealt
The Timer will no longer break from Bleed Simulation
Tree feller no longer "damages" saplings
Bleed+ (Serrated Strikes) lasts 5 ticks down from 12
Bleed/Bleed+ now do 2 damage instead of 1
Power Level is now based on permissions
Counter Attack added to swords
Parry is now based directly on Swords skill level
Parry maximum proc chance raised to 30% from 20%
Serrated Strikes now properly applies Bleed+ to targets
Players who parry can no longer be disarmed
Acrobatics now has a Dodge passive skill reducing damage
Repair skill now effects how much durability is restored
Super repair now doubles the repair amount on proc
Unarmed now starts with a bonus to damage to encourage use
Unarmed now has two steps to damage scaling, Appentice, and Mastery
Unarmed disarm now caps at 25% for 1000 skill
Fixed problem where Archery skill procs would ignore other plugins
Ignition changed to 25% chance
Ignition length will be based on archery skill level
/myspawn now has a warning about the inventory loss penalty in /mcc
mcMMO Timer now runs in 1 second intervals rather than 2

Version 0.9.10
Party invites now show who they are from
Mushrooms added to Dirt/Grass excavation loot tables, drops with 500+ skill
mcMMO configuration files property setting names have been changed for readability
Fixed bug where Gold and Iron wouldn't drop anything during Super Breaker
Added /mcability info to /mcc
Potentially fixed NPE error when checking players for being in same party for PVP XP
Removed sand specific diamond drop from sand excavation loot table, Diamonds can still drop globally for sand
Added a global XP gain multiplier, increase it to increase XP gained
Reduced PVE XP for Unarmed, now identical to Axes/Swords
Changed Chat priority in mcMMO to be higher, this should help plugin conflicts
Mushroom XP raised to 40 from 10
Flower XP raised to 10 from 3

Version 0.9.9
Fixed problem where entities never got removed from the arrow retrieval list of entities

Version 0.9.8
EntityLiving shouldn't be cast to entities that are not an instance of EntityLiving
Added a null check in the timer for players being null before proceeding

Version 0.9.7
Procs/XP Gain will no longer happen when the Entity is immune to damage (Thanks EdwardHand!)
Axes critical damage versus players reduced to 150% damage from 200% damage
Fixed bug where Daze might not proc
Changed archery Daze to follow smooth transition
Added archery Daze chance info to /archery
Cooldown lengths are now customizable, they are in seconds and multiplied by 2 by mcMMO

Version 0.9.6
Timer checks for player being null before adding them to the mcUsers system
Cooldowns will now show how much time is remaining when trying to use their respective abilities
SkullSpliiter will now correctly inform the player when they are too tired to use it
Acrobatics will no longer give XP if the event was cancelled by another plugin
Version 0.9.5
Super Breaker now gives a chance for Triple Drops based on mining skill
Ability durability loss down from 15 to 2
Ability durability loss is now toggle-able
Ability durability loss can be adjusted in the configuration file
Mining Picks are no longer lowered after activating Super Breaker

Version 0.9.4
Flowers won't drop wheat anymore
Signs won't trigger ability readiness anymore
Version 0.9.3
Bug stopping abilities from never wearing of may have been fixed
Changed color of "X Ability has worn off" to RED from GRAY
Super Breaker, Giga Drill Breaker, and Tree Feller now damage the tool significantly during use
Netherrack and Glowstone now give Mining XP
Netherrack and Glowstone are now effected by Super Breaker
Abilities will no longer be readied when you right click signs or beds
Chimaera Wings won't activate on blocks you can interact with and signs
Abilities now adjust their effects depending on tool quality
Superbreaker won't break things that tool couldn't normally break
Giga Drill Breaker will only give triple xp and triple drops for diamond tools, with a reduced effect for lesser tools
Skull Splitter now has a limit of opponents nearby it will strike based on your tool quality
Serrated Strikes now has a limit of opponents nearby it will strike based on your tool quality
Modified /mcmmo description to be a little bit more relevant.

Version 0.9.2
Changed priority of some of the mcMMO listeners
Now when certain abilities are activated it shouldn't say "You lower your x"

Version 0.9.1
Fixed "Unknown console command" errors with CB 556
Added /mcability command to toggle being able to trigger abilities with right click
Added some more nullchecks for people reporting NPE errors
Compatibility with NPC mods improved (Mainly for archery!)
Other plugins can now call inSameParty() from mcMMO to increase compatibility

Version 0.9
--NEW CONTENT--
Woodcutting now has the "Tree Feller" Ability
Unarmed now has the "Berserk" Ability
Swords now has the "Serrated Strikes" Ability
Mining now has the "Super Breaker" Ability
Axes now has the "Skull Splitter" Ability
Excavation now has the "Giga Drill Breaker" Ability
Added /mcrefresh <playername> - tool for refreshing cooldowns
Unarmed now has the "Deflect Arrows" passive skill
Chimaera Wing Item Added

--CHANGES--
HP Regen & Bleed are back
Woodcutting will drop the appropriate log on double drop procs
Herbalism now applies double drops to herbs
/<skillname> now shows much more information to the player regarding their stats
Axes skill Critical Strikes are now based directly on your skill level
Swords skill Bleed chance is now based directly on your skill level
Unarmed disarm chance is now based directly on your skill level
Acrobatics now gives XP when you roll

--BUGFIXES--
Memory Leak Fixed
Axes not doing critical strikes
Gold Armor repair
Capped skills now have the correct proc chance
/mmoedit is no longer case sensitive
More NPE errors fixed
Many bugs I forgot to write down

--PLUGIN COMPATABILITY FIXES--
If combat interactions are cancelled by other plugins mcMMO should ignore the event
If block damage interactions are cancelled by other plugins mcMMO should ignore the event

Version 0.8.22
	Fixed bug where Axes did less damage than normal
	Acrobatic rolls now give XP
	Acrobatics XP increased for non-rolls
Version 0.8.21
	Fixed bug where axe criticals would dupe items
Version 0.8.20
	99.99% sure I fixed anvils that suddenly stop working
Version 0.8.19
	Fixed being able to excavate placed blocks
	Added toggle option to mining requiring a pickaxe
	Added toggle option to woodcutting requiring an axe
	PVP interactions now reward XP based on the damage caused (this is effected by skills)
	PVP XP gain can be disabled in the configuration file
	PVP XP has a modifier, increase the modifier for higher XP rewards from PVP combat
Version 0.8.18
	Fixed sandstone not being watched for exploitation
Version 0.8.17
	mcmmo.users moved to plugins/mcMMO/
	Snowballs and Eggs will no longer trigger Ignition
	Loot tables for excavation adjusted
	Mining benefits now require the player to be holding a mining pick
	Woodcutting benefits now require the player to be holding an axe
Version 0.8.16
	Moved configuration file to /plugins/mcMMO
	Arrows now have a chance to Ignite enemiesw
	Fixed arrows not being retrievable from corpses
	Added info about ignition to /archery
Version 0.8.14
	Mining, Woodcutting, Herbalism, and Acrobatics proc rates now are based on your skill level directly rather than tiers you unlock via skill levels
	Archery's ability to retrieve arrows from corpses now is based on your skill level directly rather than tiers you unlock via skill levels
	Mining, Woodcutting, Herbalism, Archery, and Acrobatics now show their proc % relative to your skill if you type /<skillname>
	You can now adjust what level is required to repair diamond in the configuration file
	Changed mining XP rates to be a tad higher for some things
	You can now get XP from sandstone
	XP rates increased for gathering glowstone with excavation
	XP rates increased a bit for excavation
	Skill info is now a bit more detailed for certain skills
	Added info about arrow retrieval to /archery
Version 0.8.13
	Enemies no longer look like they have frozen when they die
	Item duping fix
Version 0.8.11
	Performance improvements
	Memory leak fixed
	NPE error with MySpawn really fixed
Version 0.8.9
	Fixed NPE for My Spawn
	Fixed NPE for onBlockDamage
	Bleed proc now correctly checks for Swords permissions
Version 0.8.8
	Gold can now be repaired
	Tweaked Mining XP gains
	Reorganized code
	Added /mcgod godmode command
	Fixed the pvp toggle in the settings file
Version 0.8.7
	Removed packet-sending stuff wasn't working anyways
	Fixed another NPE with the TimerTask
	Skills now only show up in /stats if you have permissions for them
Version 0.8.6
	Added a null check in bleed simulation to prevent a NPE
Version 0.8.5
	Players are now added to files when they connect (to fix a NPE)
	onPlayerCommand stuff moved into onPlayerCommandPreprocess
Version 0.8.4
	Fixed another nullpointer error for TimerTask
	Fixed bug making regeneration take twice as long to kick in after combat
Version 0.8.3
	Modified the timer intervals (from 1 second to 2)
	All skills now have an individual modifier (Set by default to 2)
	There is now a global XP modifier (Set by default to 1)
	Herbalism now correctly follows its skill curve
	Unarmed no longer gives experience for harming other players
	Players can no longer exploit mob spawners for experience
Version 0.8.2
	Fixed Concurrent Modification Exception
	Fixed some incorrect skill descriptions
	First tier of HP Regeneration is now available from the start
	Fixed bleed proc rate for very high skill levels
	Changed regeneration permissions to 'mcmmo.regeneration'
Version 0.8
	Archery skill now lets players recover arrows from downed foes
	Health regenerates based on power level
	Added toggle to myspawn clearing player inventory in settings file
	Swords now have a bleed effect
	Rewrote Skill descriptions to be more informative/better
Version 0.7.9
	XP Curve now follows a new formula
	Acrobatics XP gains changed
	Compiled against permissions 2.1
Version 0.7.8
	Massive tweaks to XP gain for Archery, Swords, Axes, Unarmed
Version 0.7.7
	Minor tweak to how players are added to the flat file
	Fixed some nullpointer exceptions when players die
Version 0.7.6
	Fixed being able to repair diamond armor with below 50 skill
	Myspawn now supports multiple worlds, clearing myspawn will set it to the first world created by the server
Version 0.7.5
	Removed random checks for herbalism XP
	Herbalism is now called properly (This should fix gaining no xp or double drops)
Version 0.7.4
	Work around for a bukkit bug that broke my onBlockDamage event
	Added /clearmyspawn
Version 0.7.3
	Fixed to work with build 424 of CB
	Lowered the XP of gold due to it not being that rare anymore
Version 0.7.2
	Fixed security flaw where players could access /mmoedit if the server was not running permissions
	Reduced XP gain of woodcutting a bit
Version 0.7
	Completely rewrote the XP system
	Added an XP skillrate modifier to the settings file

Version 0.6.2
	Axes now do critical strikes against farm animals
	Removed the "Stupidly Long Constructor"
	Now compatible with the latest CB builds
Version 0.6.1
	Customizable command names
	Axes can now be modified with /mmoedit
	Party members are now correctly informed when you leave the party
	Fixed incorrect commands in /mcc
Version 0.5.17

	Changed namespaces to fit bukkits new standard
	Adjusted excavation proc rates
	Modified excavation loot tables
	Added Party Invite System

Version 0.5.16

	Fixed unarmed not checking for permissions when hitting players

Version 0.5.15
	Fixed stone swords not being recognized as swords
	Fixed /a not working if you were an op but did not have permissions

Version 0.5.14
	Added permissions for skills

Version 0.5.13

	Removed skillgain from succesful parries
	Repair now refreshed the inventory

Version 0.5.12

	Fixed being able to hurt party members with the bow and arrow

Version 0.5.11

	Added /mmoedit command
	Fixed bug preventing player versus player damage
	Fixed bug preventing damage from scaling with unarmed & bows
	Fixed disarm proc making the opponent dupe his/her items
	Added mcmmo.tools.mmoedit permission
	Added mcmmo.commands.setmyspawn permission
	Added totalskill to /stats
	Changed the look of /stats

Version 0.5.10

    Fixed trying to set health to an invalid value

Version 0.5.9

    Fixed duping inventories on death

Version 0.5.8

    Fixed bug where players inventories would dupe during combat
    
Version 0.5.7

    Fixed monsters instant killing players
    Misc fixes
Version 0.5.4

    Changed herbalism skill gain from wheat to be WAAAAY slower

Version 0.5.3

    Players will now correctly drop their inventories when killed by a monster

Version 0.5.2

    Fixed MAJOR bug preventing swords skill from gaining through combat

Version 0.5

    Archery Added
    Swords Added
    Acrobatics Added
    Logging for Party/Admin chat added
    Fixed whois to show correct values for Excavation
    Made death messages much much more specific

Version 0.4.4

    Fixed being able to repair full durability iron tools
    Fixed herbalism benefits not behaving properly
    Fixed removing 1 diamond from every stack of diamond when repairing diamond

Version 0.4.2

    Removed myspawn from the motd

Version 0.4.1

    Fixed /mcc showing incorrect command for herbalism
    Changed unarmed skillrate to be much slower than before
    Modified a few skill descriptions
    Added permission for /whois
    Players can now use admin chat without being op as long as they have the correct permission (requires Permissions)

Version 0.4

    Permissions support
    Removed OPs having different names than normal players
    Removed /setspawn & /spawn
    Slowed down excavation skill rate
    Fixed excavation coal drop being too rare

Version 0.3.4

    Creepers now give double xp for unarmed
    Iron armor can now be repaired!
    Fixed bug stopping items from being repaired

Version 0.3.3

    Yet another herbalism skill gain tweak

Version 0.3.2

    Changed excavation loot tables to be more rewarding
    Changed sand to give normal excavation xp instead of double xp
    Fixed herbalism skill exploit
    Mobs killed with unarmed now drop loot properly
    Unarmed xp rate depends on mob (zombies lowest fyi)
    Huge player crashing bug fix on disarm!

Version 0.3.1

    Fixed excavation not saving properly
    Fixed repair using excavation values

Version 0.3

    Unarmed skill
    Herbalism skill
    Excavation skill
    Many bugfixes (thanks for reporting them!)
    /<skillname> - Detailed information about skills in game

Version 0.2.1

    Misc bugfixes

Version 0.2

    Repair ability added
    Repair skill added
    Iron Armor repair temporarily disabled
    Anvils (Iron Block) added
    /mcmmo & /mcc added
    Misc changes to existing commands
    Misc bug fixes

Version 0.1

    Releasing my awesome plugin
