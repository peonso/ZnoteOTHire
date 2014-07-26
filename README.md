ZnoteAAC for OTHire
========

original ZnoteAAC repository [GitHub](https://github.com/Znote/ZnoteAAC)

Based in ZnoteAAC 1.5 from 24/07/2014

This version is converted to work with OTHire [GitHub](https://github.com/Znote/ZnoteAAC)

Was tested with OTHire 0.0.2 compiled with `__OLD_GUILD_SYSTEM__`

* There isn't `name` in `accounts` table, changed everything that calls for `name` to call `id` instead
* Handle Kills as TFS_03
* Handle Group_id as TFS_03 (no `type` in `account` tables)
* Could not display premmium days at account, fucking $user_data['premend'] does not work.
* Changes regarding `guilds` (`creationdata` -> `creationdate`; `ownerid` -> `owner_id`)
* Others thing handled as default or TFS_02
* Houses.php stole from [HERE](http://otland.net/threads/znote-aac-converted-to-7-6-servers.217823/) (kind buggy)
* Added some tables to .../engine/database/connection.php to force compatibility