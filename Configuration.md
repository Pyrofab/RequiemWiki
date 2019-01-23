Dissolution allows a fair deal of customization through the config file.

Most of the available options should be fairly understandable in the config file but just in case, here are details.

# Client

## useShaders

*Dissolution* uses a very basic shader to render the blueish screen effect when in soul mode. If this causes issues with your installation, you can disable it.

**values :** [true, false]

**default :** false

# General

## cancelPossessingAmbientSounds

If enabled, this option will prevent any possessed entity from emitting ambient sounds. This can be convenient if the constant sounds emanating from yourself are driving you crazy.

**values :** [true, false]

**default :** false

## forceRemnant

If set to anything other than `default`, will force players' remnant status and prevent the dialogue from appearing. 

**values :** [true, false, default]

**default :** default

## technicianDialogue

If this config option is enabled, the little dialogue at the beginning of the game is replaced with an explicit if somewhat snarky user agreement prompt.

**values :** [true, false]

**default :** false

## warpyFlesh

Makes human flesh consumption add warp if *Thaumcraft* is installed.

**values :** [true, false]

**default :** true

# Ghost

These settings affect the gameplay of incorporeal players.

## allowStuckCommand

Soul players may find themselves stuck because of their limited abilities. Dissolution provides the `/dissolution stuck` command, which acts as a `/home` for soul players. You can disable that command if you so choose.

**values :** [true, false]

**default :** true

## invisibleGhosts

By default, ghosts will be translucid and the mod will simulate technical invisibility through unconventional means. If you don't want ghosts to be seen by other players or if other mods don't interact well, you can enable vanilla invisibility for ghost players.
**values :** [true, false]
**default :** false

## soulInteractableBlocks

A whitelist of blocks that ghosts can use or break. Note that special blocks from Dissolution do not need to be in this whitelist. 

**values :** a list of blocks that a ghost player will be able to interact with.
**default :** lever, glass_pane

# Respawn
## respawnInNether
If this setting is enabled, all players will get teleported to the nether upon respawn. In this case, going to the origin of the world will teleport them to their spawnpoint with a new body.
**values :** [true, false]
**default :** false

## respawnDimension
This setting is only used if `respawnInNether` is set to true. It allows modpack makers to choose a dimension for respawning as a soul. You could, for example, use it with RFTools Dimensions to create a custom judgement space or to give some kind of special challenge before letting the player resume their game.
**values :** the dimension ID you want players to respawn into
**default :** -1

## skipDeathScreen
A boon for the impatients, if this setting is enabled, players will skip the death screen and become a ghost at the place and time of their death. Death-related logic is still applied, however custom respawn behaviour from other mods is not supported. To prevent absolute cheese, using this with WoWLikeRespawn will teleport the player to their spawnpoint.
**values :** [true, false]
**default :** true