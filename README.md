# Pioneers Startup Scripts (1.0)
Alternate startup scripts for the game Pioneers - uses the "screen" command to manage session. This also restarts the Pioneers server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/PioneersSTartup) - [Official Forum](https://gameplayer.club/index.php/forum/linux-operators-scripts) ![Pioneers Mac Image](https://gameplayer.club/PioneersMac.jpg) 

[![Visit our IRC channel](https://kiwiirc.com/buttons/irc.freenode.net/PioneersFans.png)](https://kiwiirc.com/client/irc.freenode.net/?nick=guest|?#PioneersFans)

---
These start up the Pioneers game server at boot time with a "screen" process.

1. Copy **pioneers** into **/etc/init.d** - make sure it is executable
2. Copy **startpioneers** into **/OurPioneers** - make sure it is executable
3. Run "**systemctl enable pioneers**" (only needed once, will stick)
4. Run "**systemctl start pioneers**" - starts Pioneers without restarting the whole server

When you want to view the Pioneers console, just enter "**screen -r**" in your shell.

To disconnect from the Pioneers console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /OurPioneers/nostart**". To reenable it type "**rm /OurPioneers/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
