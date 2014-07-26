ZnoteAAC for OTHire
========

original ZnoteAAC repository [GitHub](https://github.com/Znote/ZnoteAAC)

This version is converted to work with OTHire [GitHub](https://github.com/Znote/ZnoteAAC)

Was tested with OTHire 0.0.2 compiled with `__OLD_GUILD_SYSTEM__`

* There isn't `name` in `accounts` table, you need to change everything that calls for `name` to call `id` instead
* Handle Kills as TFS_03
* Handle Group_id as TFS_03 (no type in account tables)
* Could not display premmium days at account, fucking $user_data['premend'] does not work.
* Changes regarding guilds (creationdata -> creationdate; ownerid -> owner_id;
* Others thing handled as default or TFS_02
* Houses.php stole from [HERE](http://otland.net/threads/znote-aac-converted-to-7-6-servers.217823/) (kind buggy)
* Added below text to .../engine/database/connection.php

CREATE TABLE IF NOT EXISTS `guild_wars` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `guild1` int(11) NOT NULL DEFAULT '0',
  `guild2` int(11) NOT NULL DEFAULT '0',
  `name1` varchar(255) NOT NULL,
  `name2` varchar(255) NOT NULL,
  `status` tinyint(2) NOT NULL DEFAULT '0',
  `started` bigint(15) NOT NULL DEFAULT '0',
  `ended` bigint(15) NOT NULL DEFAULT '0',
  PRIMARY KEY (`id`),
  KEY `guild1` (`guild1`),
  KEY `guild2` (`guild2`)
)

ALTER TABLE guilds
  ADD motd varchar(255) NOT NULL;