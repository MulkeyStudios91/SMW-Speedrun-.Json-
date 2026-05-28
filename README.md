[README.md](https://github.com/user-attachments/files/28334646/README.md)
\# Super Mario World Speedrun JSON Files



This repository contains `.json` files for Super Mario World speedrun autosplitting routes.



These files are made for use with Super Mario World speedrunning setups, especially LiveSplit/autosplitter setups that load route-specific JSON files.



\## About This Repository



This repo is for storing and sharing Super Mario World speedrun JSON files.



The goal is to keep the files organized, easy to download, and easy to update when routes or autosplit behavior changes.



These files may include setups for:



\- 11 Exit

\- 96 Exit

\- Auto start / auto end only

\- Testing or experimental versions



\## Important Game Name Rule



The file name can be different depending on the route, but inside each JSON file the game value should stay exactly:



```json

"game": "Super Mario World"

```



Do not change that value unless you know your autosplitter setup specifically requires something different.



\## How to Download a JSON File



1\. Click the `.json` file you want to use.

2\. Click the \*\*Raw\*\* button.

3\. Right-click the page.

4\. Choose \*\*Save As\*\*.

5\. Save the file somewhere easy to find on your computer.



Recommended folder example:



```text

Documents/Speedrun Files/Super Mario World/

```



\## How to Use These Files



1\. Download the `.json` file for the route you want.

2\. Open your LiveSplit/autosplitter setup.

3\. Make sure your Super Mario World autosplitter is installed and working.

4\. Load or select the `.json` file for the route you are running.

5\. Make sure your emulator, console, or USB2SNES/QUsb2SNES connection is working.

6\. Test the file before doing serious attempts.



\## Recommended Testing



Before using one of these files for real runs, test it in practice first.



Check that:



\- The timer starts correctly.

\- Normal exits split correctly.

\- Secret exits split correctly.

\- Boss exits split correctly.

\- Star World exits split separately when they are supposed to.

\- The final split/end trigger works correctly.

\- No two exits split at the same time unless that is intended.



\## Common Issues



\### The timer does not start



Check that:



\- The autosplitter is connected.

\- The correct JSON file is loaded.

\- Your emulator or console connection is working.

\- The game is actually being read by the autosplitter.



\### A split happens at the wrong time



This usually means one of the route conditions may need to be adjusted.



Possible causes:



\- Wrong level ID

\- Wrong exit trigger

\- Normal exit and secret exit using overlapping conditions

\- Boss exit using a different memory value than expected

\- Route file made for a different category



\### Two splits happen at the same time



This usually means two exits share part of the same condition.



For example, a normal exit and secret exit may both be checking the same value without enough extra information to separate them.



\### A split never happens



This usually means the JSON file is checking the wrong value, wrong level ID, or wrong exit condition for that part of the route.



\## File Organization



Files may be organized by route.



Example:



```text

11-exit/

96-exit/

testing/

```



Or they may be stored in the main folder if there are only a few files.



\## Suggested File Names



Examples:



```text

smw\_11exit.json

smw\_96exit.json

smw\_96exit\_autostart\_end.json

smw\_96exit\_testing.json

```



The file name is only for organization. The important part is that the JSON itself is correct.



\## Notes for Speedrunners



These files are provided as route tools for Super Mario World speedrunning.



They may not work correctly if:



\- Your autosplitter setup is different.

\- Your emulator/core is different.

\- Your console connection is not reading memory correctly.

\- The route uses different rules.

\- The JSON file has been edited incorrectly.



Always test before doing real attempts.



\## Updates



Files may be updated over time as issues are found or routes are improved.



If something splits incorrectly, make sure you are using the newest version of the file.



\## Credits



Created and maintained by Mulkey Studios / CookieGames1991.



These files are for Super Mario World speedrunning and autosplitting.

