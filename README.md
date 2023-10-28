soop's basic guide
=====================================================
how to run server
1) open tf2
2) run start.bat in C:\db-server\server\start.bat
3) open community server browser, and click on lan
4) join your server!

in game commands
- sm_fov // change your fov

general notes
- speed conversion is 25 units/1mph
- atm, some plugins are fucked up. i plan to remove those.

setting file changes
- C:\db-server\server\tf\addons\sourcemod\configs\dodgeball\general.cfg
	- desc: many parameters for changing the behavior of the rocket amongst other commands
	- "speed"                  "950"    // BLW ADV starting rocket speed (40mph)
    - "speed increment"        "300"    // BLW ADV increment speed (13mph)
	- "no. players modifier"   "0"      // PLEASE TURN TO 0. else rocket speed is not consistent.
    - "no. rockets modifier"   "0"      // PLEASE TURN TO 0. else rocket speed is not consistent.
	- "common%"                "100"    // only normal rockets
    - "nuke%"                  "0"      // disable the nuke

- C:\db-server\server\tf\cfg\sourcemod\dodgeball_enable.cfg
	- desc: this exec file runs when your server launches (when db is enabled)
	- sv_cheats 1	                    // allows you to use "buddha" command so you don't die to bot
	- net_fakelag 50                    // this value adds artifical ping by ms. change value to match whatever server you are used to

- C:\db-server\server\tf\cfg\sourcemod\superbot.cfg
	- desc: this file lets you change the behavior of the super bot
	- sm_bot_orbittime_max "1"          // reduces time bot orbits for... bc fuck that lmao
	- sm_bot_orbitspeed "200"           // reduces the max speed (mph) the bot can orbit... bc once again fuck that 
	- sm_bot_vote_delay "10.0"          // reduce time inbetween pvb votes. if private server this is fine, if public server, please increase back to default of 60.
	- sm_botname "Sooper Bot"           // bc funny