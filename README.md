soop's basic guide
=====================================================
## How to run server
1) open tf2 (you can also do step2 first)
2) run start.bat in C:\db-server\server\start.bat
3) open community server browser, and click on lan (may need to refresh)
4) join your server!

## Maintenance
- If TF2 has a game update, you must also update your server by running the update.bat script found in the root directory.

## In-game Commands
- this server has plugins for...
- 	!fp
- 	!tp
- 	!fov [num]

## Server Configuration
- Speed conversion is 25 units/1mph
- C:\db-server\server\tf\addons\sourcemod\configs\dodgeball\general.cfg
	- desc: many parameters for changing the behavior of the rocket amongst other commands gamemode rules
	- "speed"                  "950"    	// BLW ADV starting rocket speed (40mph)
    	- "speed increment"        "300"    	// BLW ADV increment speed (13mph)
	- "no. players modifier"   "0"      	// PLEASE TURN TO 0. else rocket speed is not consistent.
    	- "no. rockets modifier"   "0"      	// PLEASE TURN TO 0. else rocket speed is not consistent.
	- "common%"                "100"    	// only normal rockets
    	- "nuke%"                  "0"      	// disable the nuke

- C:\db-server\server\tf\cfg\sourcemod\dodgeball_enable.cfg
	- desc: runs when your server launches. insert any server commands here 
	- sv_cheats 1	                    // allows you to use "buddha" command so you don't die to bot
	- net_fakelag 50                    // this value adds artifical ping by ms. change value to match whatever server you are used to
	- mp_idledealmethod 0		
	- mp_idlemaxtime 0
	- mp_timelimit 0
	- mp_winlimit 0
	- mp_maxrounds 0 

- C:\db-server\server\tf\cfg\sourcemod\superbot.cfg
	- desc: this file lets you change the behavior of the super bot. 
	- sm_bot_orbittime_max "1"          // reduces time bot orbits for... bc fuck that lmao
	- sm_bot_orbitspeed "200"           // reduces the max speed (mph) the bot can orbit... bc once again fuck that 
	- sm_bot_vote_delay "10.0"          // reduce time inbetween pvb votes. if private server this is fine, if public server, please increase back to default of 60.
	- sm_botname "Sooper Bot"           // bc funny

other helpful links
- https://gamebanana.com/mods/12415 (remove smoke trails)
- https://github.com/lxnx-fr/tf2 (more DB plugins)
- https://github.com/flawfree/tfdbqol (snowball trail)
