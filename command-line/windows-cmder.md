## Windows - Cmder

<img src='http://making-the-internet.s3.amazonaws.com/sysadmin-cmder@2x.png' style='max-width:920px; width:100%'>

*Cmder* is a Windows front-end for the standard Windows Command Shell (aka `cmd.exe`).

In this course, we'll use a special build of Cmder that has the following benefits/customizations:

+ Uses a version of Cmder that is tested across multiple systems
+ Includes [`elevate`](http://code.kliu.org/misc/elevate/) to easily run commands as an admin
+ Includes `nano`, a simple CL text editor

<strong style='background-color:yellow; display:block; padding:5px;'>
Download the dwa15 build of Cmder:<br> <a href='https://github.com/susanBuck/cmder/archive/master.zip'>https://github.com/susanBuck/cmder/archive/master.zip
</a>
</strong>


## Installing
Cmder is designed as a "stand-alone" application, meaning it can be run from any directory on your computer. While most applications in Windows would live in your `C:\Program Files`, this is not a good location for Cmder since that directory requires administrative access, which will prevent Cmder from performing certain actions.

Knowing that, my reccomendation is to place Cmder in your `C:\` directory for simplicity.

To do this, right click the downloaded `cmder-master.zip` file and choose *Extract all*, then set the path to extract to to `C:\`

Extraction may take a few minutes.

<img src='http://making-the-internet.s3.amazonaws.com/sysadmin-extract-cmder@2x.png' style='max-width:400px; width:100%'>

Within the resulting extracted folder `C:\cmder-master\`, you'll see the Cmder icon you can use to launch the program.

<img src='http://making-the-internet.s3.amazonaws.com/sysadmin-cmder-in-destination@2x.png' style='max-width:602px; width:100%' alt='Launch Cmder'>

I recommend creating a shortcut to `C:\cmder-master\cmder.exe` (in your start menu, task bar, etc.) so the program is easily accessible.

That's all you need to do to get Cmder rolling. The rest of this doc includes some notes about how Cmder is customized, but requires no action on your part.


## Basic settings
Basic Cmder interface settings are done via (`Win + Alt + P`) the *Settings* menu found via the menu icon on the bottom right.


## Aliases
Aliases are stored in `/config/user-aliases.cmd`.

Run `alias name=full command` to create an alias, or edit `/config/user-aliases.cmd`.


## Creating your own commands
Create new commands via text files with the `.bat` extension inside `bin/`.

For an example, see the `alias.bat` file that creates the `alias` command.