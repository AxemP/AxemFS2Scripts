# AxemFS2Scripts
Axem's Lua Scripts for FreeSpace2 Open

Some Lua scripts to make FreeSpace missions more fun and exciting by expanding the toolbox of the mission designers.

A lot of the scripts use a JSON formatted config file. It's highly recommended you use a JSON editor (like this one: https://jsoneditoronline.org/) to edit the files. Subtle syntax errors are a giant pain!

# Base Files

These scripts contain some generic functions and libraries that are used in a number of the scripts. It's a good idea to have these installed if you're going to use any of the scripts here. (Otherwise they won't work!)

# Cloak

This script allows both the player and AI to be able to cloak. A config file (included) allows you to tweak the finer details, including if weapons or afterburner will kill the cloak, or if shields remain up. The script also includes a 'Cloaking Device' weapon that you can add to a ship's loadout, if a ship has this in their loadout they will get cloaking automatically. Otherwise a lua sexp is needed to give the cloaking ability.

2 sample missions are included

# Debug Tools

A few scripts meant to help you, the modder, with any sort of issues that may arise when making a mission or mod.

While in a mission pressing `5` will toggle a display of SEXP variables. `6` will inform you of their type, `7` will append bitmask information to the sexp variables. `8` will give some very verbose data about your current target. `9` will give that same batch of verbose data about the player's ship.

Also included is a PrintDebug() lua function for helping debug lua scripts. By inserting a table into the function, the function will recursively list the entire contents of the table. This is good to see what exactly your lua script is doing.

# In Mission Jump

This script will automatically do an in mission jump sequence to a selected waypoint for the player and AI. The lua sexp `lua-jump-to` is used to trigger this sequence. The first point on the waypoint path is used as the destination, the second point is used for orientation (relative to the first one). The sexp documentation for the sexp contains more specifics for how everything is timed. It is highly recommended that this be used with only fighters!

A sample mission is included

# Prompt Box v2

Get a player response with the prompt box! This new version does away with ugly hud gauges and now draws bitmaps directly to the screen. The method to setting up the prompt box is now made much easier with a single lua sexp being able to initialize, set options, and populate the list of responses. Recalling player responses are now also much easier. Prompt Box v2 should be fully compatible with previous versions. See sexp documentation and the sample mission for more insight into how it all works.

A sample mission is included
