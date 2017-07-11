Dissolution allows heavy customisation through the config file.

Most of the available options should be fairly understandable in the config file but just in case, here are details.

# Version
**Do not mess with this number !** It is used by the mod to automatically update the configuration file when some changes are needed.

# Respawn
The (currently) most customisable part of the mod. 

## WoWLikeRespawn
This setting forces a corpse to spawn when a player dies. This corpse will last 5 minutes, which means the player will have to reach it as a soul in this lapse of time if they want to get their stuff back. They still have all the other respawn options available. This setting should make stuff retrieval easier than vanilla (as you cannot die on the way to your stuff).
values : [true, false]
default: disabled

## playerBodiesHoldInventories
This setting controls whether player inventories will get transferred to long-lasting corpses, letting them act as some sort of gravestone. (Keep in mind that, unlike gravestones, corpses can decay over time)
values : [true, false]
default: enabled

## shouldRespawnInNether
If this setting is enabled, all players will get teleported to the nether upon respawn. In this case, going to the origin of the world will teleport them to their spawnpoint with a new body.
values : [true, false]
default: disabled

## respawnDimension
This setting is only used if shouldRespawnInNether is set to true. It allows modpack makers to choose a dimension for respawning as a soul. You could, for example, use it with RFTools Dimensions to create a custom judgement space or to give some kind of special challenge before letting the player resume their game.
values : the dimension ID you want players to respawn into
default: -1

## skipDeathScreen
A boon for the impatients, if this setting is enabled, players will skip the death screen and become a ghost at the place and time of their death. Death-related logic is still applied, however custom respawn behaviour from other mods is not supported. To prevent absolute cheese, using this with WoWLikeRespawn will teleport the player to their spawnpoint.
values : [true, false]
default: false

# Ghost
These settings affect the gameplay of incorporeal players.

## flightMode
This setting will allow you to change the way you fly as a ghost. Keep in mind that you need experience to use most of these.
values : [-1 (no flight at all, discouraged as the rest of the mod assumes you can)
          0  (custom flight, lets you glide *even with no xp* and provides a good deal of mobility. You should probably avoid fluids.)
          1  (creative flight, just double tap jump to toggle)
          2  (spectator-lite flight, you are always flying. Noclip is disabled though)]
default: 0

## invisibleGhosts
By default, ghosts will be translucid and the mod will simulate technical invisibility through unconventional means. If you don't want ghosts to be seen by other players or if other mods don't interact well, you can enable vanilla invisibility for ghost players.
values : [true, false]
default: false

## soulInteractableBlocks
A whitelist of blocks that ghosts can use or break. Note that special blocks from Dissolution do not need to be in this whitelist. *This config is not currently taken into account*.
values : a list of blocks that a ghost player will be able to interact with.
default: lever, glass_pane

# General
## doSablePop
By default, the extractor will spawn its output stacks in the world if it cannot output in an appropriate container. This behaviour can be toggled to prevent needless lag. *don't ask about the name please*
values : [true, false]
default: true

## minionsAttackCreepers
We are a bit sadistic in the team, so your freshly resurrected johnny will probably attempt to defend you from creepers. Skeleton minions might have a chance, others not so much.
This config option might let you preserve your minions for a few more instants.
values : [true, false]
default: true
