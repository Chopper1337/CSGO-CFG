# Chopper's Counter-Strike: Global Offensive Configuation
My CSGO config, based on [Budi's config](https://gist.github.com/nickbudi/3916475).

This config is by "Chopper" not "[chopper](https://liquipedia.net/counterstrike/Chopper)", difference is he's pro, I'm not :))))
 
 Here's his settings [ProSettings.net](https://prosettings.net/counterstrike/chopper/)
# Info
Note that the binds in this CFG are created around the QWERTY UK/Ireland keyboard layout

**Last update**: 13/06/21

 **Mouse**: 1khz polling rate, 800dpi, 6/11 Windows sens. and 0.9 in game sens. ([Logitech G PRO Wired](https://www.amazon.co.uk/gp/product/B07L9FJS98))
 
 **Video**: 1920x1080, 144hz, All settings on lowest, Uber Shaders enabled ([Benq Zowie XL2411P](https://www.amazon.co.uk/BenQ-XL2411P-Sports-Adjustable-eQualizer/dp/B075JGL4WV), GTX 1080Ti)
 
# Features
* Modified rates based on ping
* Jump throw bind
* Togglable scroll B-Hop
* Warmup with bots
* Easy adjustments for game and voice volume
* Various Half Life sounds for switching weapon, pressing the use key etc. (From [FranzJ](https://www.youtube.com/watch?v=KIck3ZEXIfU))
* Radar size adjustment bind
* Clearing of decals
* Lowered GPU usage in menus
* Surf Mode
* CSS viewmodel with minimal weapon movement
* Many other adjustments...

# Installation
[**>>>>Backup your original config!<<<<**](https://youtu.be/tsXrdzcbmbM?t=30)

**1.** Download [autoexec.cfg](https://raw.githubusercontent.com/Chopper1337/CSGO-CFG/master/autoexec.cfg) and open in any text editor. 
(Optional: Download [autowelcome.cfg](https://raw.githubusercontent.com/Chopper1337/CSGO-CFG/master/autowelcome.cfg) and [video.txt](https://raw.githubusercontent.com/Chopper1337/CSGO-CFG/master/video.txt))

**2.** Change `cl_interp` and `cl_interp_ratio` according to your average ping, following this table:

| Ping (ms) | cl_interp | cl_interp_ratio    |
|-----------|-----------|-------------------|
| 1-29      | 0.007813  | 1 |
| 30-59     | 0.015625  | 1 |
| 60-89     | 0.015625  | 2 |
| 90-100    | 0.03125   | 2 |

**Note**: You can find your average ping on Valve servers by going to the "Latency" tab in your "Personal Game Data" for CSGO through the games list on your profile.


**3.** Change `hud_scaling` in the "HUD" section (Line 91) according to your preference.

**4.** Modify or delete the crosshair section (Line 136). [View crosshair](https://github.com/Chopper1337/CSGO-CFG/raw/master/Screenshots/0screenshot.jpg)

**5.** Save and drop the autoexec.cfg (and autowelcome.cfg ) into the following directory
`\Counter-Strike Global Offensive\csgo\cfg\`<br>
(Default location:
`C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\csgo\cfg\`)

If you downloaded [video.txt](https://raw.githubusercontent.com/Chopper1337/CSGO-CFG/master/video.txt), place it in
`\Steam\userdata\[YOUR USER ID]\730\local\cfg`

Buy binds can be generated on [CSGOBindsGenerator.com](http://csgobindsgenerator.com/)

Changes should be automatically applied on game launch.

If you change a setting through console while in game, you can press the **Delete** key to re-run the autoexec.cfg (or type "exec autoexec" in console) to revert to the setting specified there.

# Launch Options

`-nojoy -novid  -tickrate 128 -console -high +cl_updaterate 128`

Disables controller and startup videos.

Changes default tick rate to 128, this means matches you host (such as 1v1s) will be 128 tick.

Sets the game's priority to High priority.

**Optional extras**: 

`-nogammaramp` Will remove any in-game brighness/gamma adjustments. Increases contrast which makes it easier to see players in bright situations but may cause players blend into dark backgrounds. 

`-threads #` Sets the number of CPU threads the game should try use, replace `#` with number of threads.

`-useforcedmparms -noforcemspd -noforcemaccel` If you really want to be sure there's no mouse acceleration

`-r_emulate_gl` "Emulates OpenGL on Windows, provides a framerate boost for most GPUs " - Valve

**What I use**:

`-nogammaramp -novid`

Disables brightness/gamma adjustments and skips the "CSGO" splashscreen.



# Binds
**Middle click**: Toggles scroll wheel between B-Hop and weapon switching

**Insert**: Enters bot warmup

**Home**: Switch to Spectator

**Delete**: Executes autoexec.cfg

**Mouse 4, Mouse 5**: Equip Smoke or Flash

**Square Brackets**: Adjust radar zoom

**Right Shift**: Surf mode (300fps limit, mouse4 and mouse5 are mapped to turn left and right)

**Enter**: Global chat

**Backslash**: Team chat

**F2**: Re-buy last loadout

**E**: Use key

**F**: Inspects weapon

**N**: Jump throw, equip a nade, hold mouse1 and then hold N to jump throw

**T**: Equip Molotov / Show mouse on scoreboard

**L**: Toggles `cl_righthand`

**V**: Voice chat

**Z,X,C**: Radio commands

**7**: Toggles `noclip` and debug mode

**0**: Toggles `voice_enable`

**Negative/Minus**: Toggles voice_scale

**Equals**: Adjusts game volume between the following values `1 0.7 0.1 0`

**Comma**: Ping crosshair location

Probably missed some, read through the config, make your own changes

# Some visible changes

* HUD takes less space and is on bottom of screen <br>
![](https://github.com/Chopper1337/CSGO-CFG/raw/master/Screenshots/players-alive.jpg)
* Viewing the scoreboard will toggle `cl_showpos` and `net_graph` <br>
![](https://github.com/Chopper1337/CSGO-CFG/raw/master/Screenshots/scoreboard-info.jpg)
* HUD is scaled down to take up less space `hud_scaling "0.65"` and is also green for visibility `cl_hud_color "8"`<br>
![](https://github.com/Chopper1337/CSGO-CFG/raw/master/Screenshots/0screenshot.jpg)
* Optional welcome message <br>
![](https://github.com/Chopper1337/CSGO-CFG/raw/master/Screenshots/welcome%20message.jpg)

# Notes on performance for CSGO

Unless you're running a GT710, **the main thing to consider for CSGO is CPU performance**. The more utilisation the games gets of your CPU, the better your framerate will be. GPU isn't as important as all settings will be on lowest and most players are playing in a lower resolution such as 1280x960.

**CSGO doesn't seem to utilise many cores**, so 4 very fast (Clock and IPC) cores will give a good FPS.

**CPU clock speed boosting technologies** such as AMD's Precision Boost Overdrive **should be preferred over an all core overclock for CSGO**, unless you can get an all core OC higher than what PBO (or any equivalent) can provide.


Be sure that your Windows power profile is set to **High Performance** or a similar equivalent while playing to prevent CPU throttling.

**Removing bloat from your OS will help**.

**Reduce your CPU usage** as much as possible when playing CSGO. Programs such as **web browsers will use enough CPU cycles to affect your FPS** even if they're idle while you play. I recommend using a lightweight third party Discord client, such as [Ripcord](https://cancel.fm/ripcord/ "Ripcord"),  if you must use Discord for communication while you play as discord itself it just another web browser running in the background.

If you are a Windows user, **Windows 10 LTSC will run the game better** than the latest version from Microsoft. If you want as much resources put towards your own programs and games, such as CSGO, and not so much on random background telemetry and analytic programs, it's a good idea to switch to an LTSC/Enterprise version of Windows.

For Linux users, make sure you're using a kernel optimised for gaming such as [TKG](https://github.com/Frogging-Family/linux-tkg "TKG")

# Sources

[Rates (Net code)](https://steamcommunity.com/sharedfiles/filedetails/?id=795437982)

[Sound settings](https://steamcommunity.com/sharedfiles/filedetails/?id=703059693)

[FranzJ Half Life Sounds](https://www.youtube.com/watch?v=KIck3ZEXIfU)

[Budi's CFG](https://gist.github.com/nickbudi/3916475)

[Launch options (Valve)](https://developer.valvesoftware.com/wiki/Command_Line_Options)

[Launch options (Third Party)](https://totalcsgo.com/launch-options)
