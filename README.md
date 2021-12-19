# Server

Configuration files for the [Jaunty](https://jaunty.fun) server.

Jaunty runs [Paper](https://papermc.io), a fork of Spigot (a fork of Bukkit) with some plugins.

* Simple Voice Chat (93738) - Adds proximity voice chat to the game
*	* Depends on ProtocolLib (1997)
*	*	* At the time of writing, requires you to install from CI rather than Spigot (for 1.18.1)
* Chunky (81534) - Administration tool for pregenerating chunks
* Spark - Used for profiling the server

Configuration files have been tweaked to our liking, and to optimize the server. Optimizations are based off of [YouHaveTrouble/minecraft-optimization](https://github.com/YouHaveTrouble/minecraft-optimization).

All of this ran in a Docker container, using [itzg/minecraft-server], along with the companion container [itzg/mc-backup] for regular backups.

The JVM has been configured using [Aikar's flags](https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/); the heap has been given 6GB of RAM, the VPS Jaunty runs on has 8GB.
