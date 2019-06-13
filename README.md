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

1) Download Zilminer, Download your other miner (let's say Claymore), Download Zilliqa-Switcher
2) Extract all files from all three downloaded packages in the same folder.
3) Optional: Create an eth.bat script if you need to.
4) Run Zilliqa-Switcher
5) First option, choose your miner
6) Second option, choose how you run your miner, either using only exe or using a bat file (created in step 3)
7) Third option if you chose bat file, enter the name of the bat file, (eth.bat , grin.bat)
8) Forth option, enter your Zilliqa Address. This can be the old formart Zil address or New Format Zil Address
9) That's it :)

# Errors  + Solutions

If you get an error, please ensure you answered each option correctly. Else, leave an issue here with screenshots and step by step instructions on how you came about the error.

My Command Prompt screen no longer crashed/stopped doing anything. This is an issue with Command Prompt. Right click at the top of the command prompt, choose Properties, Disable Quick Edit.
To permanently fix this, choose Default instead of Properties then Disable Quick Edit.

My miner is not on the list. This project is a work in progress. If you do not see your miner of choice, please create an issue here and I will quickly add support for it.

# Work in Progress

Support for Phoenix Miner, Claymore, SRBMiner.
