# Vice City Roleplay (SA-MP 0.3.DL)
SA-MP server in Vice City created from scratch.

## Dependencias
- SA-MP 0.3.DL-R1 server (https://archive.org/download/sa-mp-0.3.dl/samp03DL_svr_R1_win32.zip)
- Pawn Compiler 3.10.8 (https://github.com/pawn-lang/compiler/releases/tag/v3.10.8)
- sscanf 2.8.2 (https://github.com/maddinat0r/sscanf/releases/tag/v2.8.2)
- GPS (https://github.com/kristoisberg/samp-gps-plugin/releases/tag/1.4.0)
- Streamer 2.9.4 (https://github.com/samp-incognito/samp-streamer-plugin/releases/tag/v2.9.4)
- MySQL R41-4 (https://github.com/pBlueG/SA-MP-MySQL/releases/tag/R41-4)
- Pawn.Regex 1.1.2 (https://github.com/urShadow/Pawn.Regex/releases/tag/1.1.2)
- samp-mysql-yinline-include v1.0.1 (https://github.com/maddinat0r/samp-mysql-yinline-include/releases/tag/v1.0.1)
- YSI 4.0.2 (https://github.com/pawn-lang/YSI-Includes/releases/tag/v4.0.2)

## Quick Installation
1. Install the dependencies.
2. Copy the includes from the *includes* folder to your Pawn compiler.
3. Create the databases using the *schemas/databases.sql* file.
4. Import each *.sql* file from the *schemas* folder into its corresponding database.
5. Compile *filterscripts/maps.pwn* and *gamemodes/main.pwn*.
6. Configure *server.cfg* if necessary.
7. Open *samp-server.exe*.

## Gamemode
*(main.pwn)*
- Comment out the line **#define LOCAL_HOST** to enable production mode.
- Redefine **#define MAX_PLAYERS 50** according to the maximum slots of your server.
- Redefine **#define SAVE_ACCOUNTS_TIME** if necessary, which is the interval for saving online accounts, by default it is **5 minutes**.
- **The radios do not work because they depend on a server; you can activate them using your own server by:**
  - Redefining **#define RADIO_URL** in the *gamemodes/server/radios/header.inc* file.

### Ignore the following compiler warnings
```
gamemodes\main.pwn(48) : warning 218: old style prototypes used with optional semicolumns
gamemodes\player/pstats/funcs.inc(167) : warning 213: tag mismatch: expected tag none ("_"), but found "Float"
gamemodes\player/label_render/funcs.inc(82) : warning 213: tag mismatch: expected tag none ("_"), but found "Float"
gamemodes\player/label_render/funcs.inc(83) : warning 213: tag mismatch: expected tag none ("_"), but found "Float"
```

