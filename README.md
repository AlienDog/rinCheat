#rinCheat
A multifunction plugin for PSVITA.

## Disclaimer

THIS TOOL HAS BEEN RELEASED JUST FOR TESTING PURPOSES. THIS IS NOT FINISHED AND THERE STILL ARE LOTS OF BUGS TO BE SOLVED. REPORT ON WOLOLO'S THREAD WHATEVER BUG YOU FIND IF YOU WANT TO CONTRIBUTE TO ITS DEVELOPMENT.

## Features

- Cheats Database support
- Real-Time Cheats with a Stack+Heap searcher+injector
- Screenshot feature with higher quality for any games
- Clockage change
- Decrypted savedata export/import
- Stack dumping/restoring
- Autosuspend hack to disable autosuspend feature of PSVITA

## How to install and use

Place rinCheat.suprx to ux0:/plugins, then open ux0:/plugins/game.txt file and add this line to the file:
ux0:/plugins/rinCheat.suprx 1
To open rinCheat menu just press SELECT+START during your game session.

## How to use (CPU Clockage & AutoSuspend)

Pretty straightforward, navigate to Game Hacks menu and then enable such features.

## How to use (Screenshot feature)

In Game Hacks menu, enable Screenshot feature then close rinCheat.
During your game sessions you'll be able to take screenshots by pressing L+R+START.
Screenshots will be saved in ux0:/data/rinCheat/screenshots.
NOTE: If you see on right-bottom side of your screen the text "MMC Mode", taking a screenshot will take a lot of time (more than a minute).

## How to use (Value searcher/injector)

Navigate to Game Cheats -> Search Value.
In this screen you'll be able to search an arbitrary value of 1,2,4,8 bytes on stack or heap.
First of all set the value you want to search and its size, then press one of the two Start Absolute Search options, you'll be prompted with how many matches has been found.
Now you can directly inject a new value by pressing Inject value or you can unpause the game and, later, search between the matches how many changed their values by using Start Relative Search feature.
You can also use the Save offsets function (RAM Mode only at the moment) to save matched offsets on ux0:/data/rinCheat/db/TITLEID_offsets.txt. These offsets can be extremely useful to actually write automated cheats to insert to rinCheat database.

## How to use (Cheats List)

rinCheat actually has no cheats database cause cheats must by found by testers. When you find a good offset with the value searcher you can save the offset to actually write a cheat that will appear in the Cheats List.
To do so, after you saved the offsets, you have to create a file in ux0:/data/rinCheat/db named as TITLEID.txt. Here you can put how many cheats you want that will appear in the Cheats List.
Syntax for the file is:

\#CHEAT NAME<br>
@offset @value @size

(Remember to put a new line at the end of the file, just a minor bug that will be solved in next releases)

Example:

\#999 Max Health<br>
@0xB1A4A231 @0x3E7 @4

## How to use (Decrypted savedata dumper/restorer)

Such features are available on main menu. Dumper will save the savedata to ux0:/data/rinCheat/TITLEID_SAVEDATA.
Edit your savedata as you wish and then you can re-inject it back by using the related feature.
