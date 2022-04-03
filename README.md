# Dead by Daylight 2.4.0 Server

## What is this?

This is a modified version of Preston's 3.0.0 Dev Build server that allows you to run Version 2.4.0 of the game.

## Why?

There is currently no way to play Version 2.4.0 of the game, and this aims to solve that.

## Installing Version 2.4.0

1. Install [DepotDownloader](https://github.com/SteamRE/DepotDownloader) and .NET 6.0.
1. Open a Command Prompt and navigate to the .dll file.
1. Run the following command, replacing the username and password placeholders with your account details (you must own a valid copy of DBD on Steam):
```
    dotnet DepotDownloader.dll -app 381210 -depot 381211 -manifest 8633017681482216550 -username <username> -password <password>
```

## How to run

1. Make sure [NodeJS](https://nodejs.org/en/) 14 and [NPM](https://www.npmjs.com/) are installed on the machine you wish to run the server on. Other versions of Node may function, but they have not been tested.
1. Make sure you have [Fiddler 4](https://www.telerik.com/download/fiddler) installed. This must be running while the server is active.
1. [Download](https://github.com/ReverseVelocity/dbd-server-2.4.0) and extract the newest release.
1. Run `setup.bat` (or `setup.sh` on Linux) to install all necessary dependencies.
1. Run `run.bat` (or `run.sh` on Linux) to start the server. NOTE: You will probably get a Version Check error, do not worry, this is normal.

## How to use

1. Go to the folder where your game is installed, and rename the Live Version of the game to something else.
1. Rename the folder Version 2.4.0 is installed to "Dead By Daylight".
1. Add the following lines to the end of DefaultEngine.ini (located in DeadByDaylight/Config).
    ```
    [/Script/Engine.NetworkSettings]
    n.VerifyPeer=false
    ```
1. Add the following entries to your HOSTS file, replacing `127.0.0.1` with the IP of the server if it isn't your local machine. Do not replace the IP in the third line, which is meant to sinkhole to 0.0.0.0 regardless of the location of the server. If you're not sure how to edit your HOSTS file, check [here](https://www.howtogeek.com/howto/27350/beginner-geek-how-to-edit-your-hosts-file/).
    ```
    127.0.0.1    latest.live.dbd.bhvronline.com
    127.0.0.1    cdn.dev.dbd.bhvronline.com
    0.0.0.0     analytic.live.dbd.bhvronline.com
    ```
1. Launch the game from Steam.

## Contributors

- [Preston](https://github.com/Preston159) - He modified the Dev Server to work with this version, I'm just uploading it to Github so anyone can use it.


# Copyright Notice

[Dead by Daylight](https://deadbydaylight.com/en)&trade; (DbD) is a trademark of [Behaviour Interactive](https://www.bhvr.com/).