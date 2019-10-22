# Zilliqa-Switcher

# Introduction

Zilliqa has developed a new way of mining compared to regular methods we all know of. POW is every 2-3 hours. That's right 2-3 hours. In that POW time, your miners only mine for 1 minute. I kid you not. This is to help the planet go green with mining but I am greedy and would like to use all the rest of time to mine something.

# Dual Mining Zilliqa 
Zilliqa miner already has a function to allow dual mining. For Zilliqa, dual mining is Mining on own coin (eth, jesus coin, grin, etc) while waiting for POW for Zilliqa. When POW is close, zilminer will stop your mining operations of eth (or any other coin you are mining) and begin to mine Zilliqa for one minute. After the minute has passed, it continues to mine your eth.

# Problem
Although dual mining Zilliqa is great, it never works out the way you expect. Unexpected issues like zilminer crashing, your eth miner crashing, heck your pc crashing have been an issue from day one. Read Solution below.


# Introducing Zilliqa- Switcher

Instead of your miners crashing, I offer you a solution to mine any other coin with any other miner while still making it in time to mine Zilliqa. This is a work in progress but it works well.

# Instructions

Miner Numbers :
Custom Scripts = 0
Phoenix Miner = 1 
Claymore = 2 
SRBMiner = 3 
SGMiner = 4 
BMiner = 5
GMiner = 6
NiceHashMinerLegacy = 7
CCMiner = 8 
TT-Miner = 9 
ewbf_144 = 10 
NBminer = 11 
Team Red Miner = 12 
Xmr-Stak = 13

# Run in Command Line 

-m or --miner    This is required to let the script miner you would like to dual mine Zilliqa with. Below are the parameters to choose from. Example, -m 15 uses LolMiner + Zil.

Custom Script = 0 ,Phoenix Miner = 1 Claymore = 2, SRBMiner = 3, SGMiner = 4, BMiner = 5, GMiner = 6, NiceHash Miner Legacy = 7, CCMiner = 8, TT-Miner = 9, ewbf_144 = 10, NBminer = 11, Team Red Miner = 12, Xmr-Stak = 13, MinerStat = 14, LolMiner = 15, NiceHash Miner = 16, T-Rex = 17

-r or --run   This is required to start your Miner (chosen with -m). Not required for custom scripts option. Either use an exe or bat. Example -r PhoenixMiner.exe  or -r start.bat

-a or --address    This is required to mine Zilliqa to your correct address. New or old format works. Example  -a 0xe511b07b68681d4501665De40cf6A734f05da94f

-w or --worker   This is your miner name for mining Zilliqa. This is optional. If left empty, it uses your PC Name


Custom Script Explanation

This is for users that would like to use their own scripts to open and close their miner of choice.

-r or --run   Is not to be used for this.

-s or --start   Used to stop your miner. This should be a bat file.  Example  -s stop.bat

-e or --end    Used to start your miner. Example -e ewbf_144.exe  or --end start.bat

But... I used the old format to run this script

We have you covered, we have added backward compatibility. When you update to the newest version, you old scripts should work (PM @kidkid1 if you have issues or PM me here)

# Examples

Example #1: zil_switcher.exe  -m 1 -r miner.bat  -a 0xe511b07b68681d4501665De40cf6A734f05da94f

Example #2: zil_switcher.exe -m 2 EthDcrMiner64.exe  -a zil1u5gmq7mgdqw52qtxthjqea48xnc9m22067k4gf

Example #3: zil_switcher.exe -m 2 EthDcrMiner64.exe -a zil1u5gmq7mgdqw52qtxthjqea48xnc9m22067k4gf -w miner1

Example #4: zil_switcher.exe -m 1  -r start.bat -a 0xe511b07b68681d4501665De40cf6A734f05da94f -w win_miner

Example #5: zil_switcher.exe -m 0 -a 0xe511b07b68681d4501665De40cf6A734f05da94f -s stop.bat -e start.bat

# Run outside of Command Line

1) Download Zilminer, Download your other miner (let's say Claymore), Download Zilliqa-Switcher
2) Extract all files from all three downloaded packages in the same folder.
3) Optional: Create an eth.bat script if you need to.
4) Run Zilliqa-Switcher
5) First option, choose your miner
6) Second option, choose how you run your miner, either using only exe or using a bat file (created in step 3)
7) Third option if you chose bat file, enter the name of the bat file, (eth.bat , grin.bat)
8) Forth option, enter your Zilliqa Address. This can be the old formart Zil address or New Format Zil Address
9) That's it :)

# For Awesome Miner

First, be sure that API is activated in Awesomeminer.
 
Screenshot

https://prnt.sc/pmgzdn
 
Zil_Switcher start commandline:
 
Zil_Switcher.exe -m 0 --wallet ******** --worker ****** -s stop.bat -e start.bat
 
Wallet and Worker not really needed, but you need it that the Zilswitcher start.
 
 
Now the 2 scripts to stop the main miner and start the Zilminer
 
start.bat
 
curl -i -d POST http://[IP_AWESOMEMINER_MAIN_PC]:17790/api/miners/[MINERID]?action=stop       #stop main miner in Awesomeminer(miniZ,Gminer,lolminer etc)
 
curl -i -d POST http://[IP_AWESOMEMINER_MAIN_PC]:17790/api/miners/[MINERID]?action=start #start zilliqa miner in Awesomeminer  
 
stop.bat
 
curl -i -d POST http://[IP_AWESOMEMINER_MAIN_PC]:17790/api/miners/[MINERID]?action=stop   #stop zilliqa miner in Awesomeminer  
 
curl -i -d POST http://[IP_AWESOMEMINER_MAIN_PC]:17790/api/miners/[MINERID]?action=start #start main miner in Awesomeminer(miniZ,Gminer,lolminer etc)

 
MinerID can found in Awesomeminer summary tab

# Screenshot

https://prnt.sc/pmgzi2

Example:
 
start.bat curl -i -d POST http://192.168.2.113:17790/api/miners/37?action=stop curl -i -d POST http://192.168.2.113:17790/api/miners/48?action=start
 
stop.bat curl -i -d POST http://192.168.2.113:17790/api/miners/48?action=stop curl -i -d POST http://192.168.2.113:17790/api/miners/37?action=start
 
Another way where you only need one miner in Awesomemine, is to change the template via API.  If needed i make a documentation.
 
I am sure, now there are so many ways. Find your own way or ask me Smiley
 
If your windows doesn´t have curl, then you find it online as portable version.

Documentation Created by sxemini https://bitcointalk.org/index.php?action=profile;u=2021959


# FAQ

I use HIVE OS.

Message @kidkid1 in telegram for scripts

My Command Prompt screen no longer crashed/stopped doing anything.

This is an issue with Command Prompt. Right click at the top of the command prompt, choose Properties, Disable Quick Edit. To permanently fix this, choose Default instead of Properties then Disable Quick Edit.

My miner is not on the list.
This project is a work in progress. If you do not see your miner of choice, please create an issue here and I will quickly add support for it.

Are there any fees to use this?
There are no fees attached.

Can I donate?
Sure

BTC: 347DrMsEhPaxVQjvrYFRoiAHb5NQoNGV7R
ETH: 0x374817E3F8adDBa6A03B7872f7CBeD0ce8C6AE8E
ZIL: 0xe511b07b68681d4501665De40cf6A734f05da94f

