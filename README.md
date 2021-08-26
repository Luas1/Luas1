- 👋 Hi, I’m @Luas1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Luas1/Luas1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
@@ -144,6 +144,7 @@ These sub-options are:
- `hide_ally_objects`: hide all objects created by other players, except for macrons. This includes, but not limited to: bullets, grenades, fire, blasts, rockets.
- `hide_effects`: hide damage effects (flashes/explosion sprites), death animations, particle trails (smoke trails, warp particles).
- `replace_shake`: replace screen shake and flash effects with an indicator in top middle of the screen.
- `hide_chat`: completely hide chat.

### `[plugin_playerlist]` - player list

@@ -168,19 +169,11 @@ Valid key names are listed here (first column, case sensitive): https://wiki.lib

One key can be bound to any amount of options, and one option can be changed by any amount of keybinds.

## Mipmaps and sprite editing
## Sprite editing

SBPE is compatible with modified sprites. However, when mipmaps are enabled, default sprite sheets are not loaded.
SBPE is compatible with sprite editing. Edit the original sprite sheets (images with long names in `data/texture/`). If enabled, mipmaps are re-generated automatically on restart whenever the original sprites are changed.

To see sprites from default sprite sheet names, disable mipmaps (`mipmaps = no`).

To re-generate mipmaps after you have edited and tested your new sprites:

- close the game
- enable mipmaps
- delete this file in the game directory: `data/texture/DataVersion.m.bpb` (note the m!)

On the next start SBPE will update mipmaps accordingly.
(Since this uses "last modified" time of the files, if you replace your sheets with a backup, it might not trigger. In this case, delete the corresponding `.m.bpb` file to re-generate that particular pack. (For example, to re-generate `base`, delete `base.m.bpb`.))

## Compiling

  2  remote.py 
@@ -11,7 +11,7 @@

util = None

VERSION = 'v1.6.1'
VERSION = 'v1.7.0'
LOGFILE = 'remote.log'
CONFIGFILE = 'config.ini'

