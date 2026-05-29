# Super Mario World Autosplit JSONs

Route JSON files for Super Mario World speedrunning autosplit setups.

These files are meant for LiveSplit autosplitting setups that can load a JSON route definition. Each file contains an autostart condition and a route-specific list of split triggers.

## Intended Setup

These JSON files are built around a console memory-reading setup, not manual splits.

The expected setup is:

- Super Nintendo / compatible console
- FXPAK Pro
- USB2SNES or QUsb2SNES connection
- LiveSplit
- LiveSplit autosplitter support
- `livesplit-usb2snes.dll` or an equivalent USB2SNES LiveSplit component

If your emulator, console connection, or LiveSplit component reads memory differently, some addresses may need testing or adjustment.

## Available Files

| Category | File |
| --- | --- |
| 96 Exit | `smw 96 Exit.json` |
| 95 Exit, No Cape | `smw_95_exit_no_cape.json` |
| All Castles | `smw_all_castles.json` |
| All Castles, No Cape | `smw_all_castles_no_cape.json` |
| All Castles, Small Only | `smw_all_castles_small_only.json` |
| No Starworld | `smw_no_starworld.json` |
| No Cape, No Starworld | `smw_no_cape_no_starworld.json` |
| No Starworld, Small Only | `smw_no_starworld_small_only.json` |
| 11 Exit | `smw_11exit.json` |
| 11 Exit, No Cape | `smw_11_exit_no_cape.json` |
| Small Only | `smw_small_only.json` |
| Lunar Dragon | `smw_lunar_dragon.json` |
| 0 Exit | `smw_0_exit.json` |

## What These Files Do

The JSON files split on game memory values. The current route files mainly use:

| Address | Use |
| --- | --- |
| `13BF` | Current level / translevel guard |
| `1493` | Normal level clear and boss clear trigger |
| `1434` | Keyhole exit trigger |
| `1609` | Bowser / final ending trigger used by the current files |

The keyhole exits use `1434 > 0` instead of the older `13CE == 0x01` check.

## Important Limitations

These files split route progress. They do not judge category rules by themselves.

For example:

- No Cape files do not check whether Cape Mario was used.
- Small Only files do not check Mario's powerup state.
- Lunar Dragon currently uses the 96 Exit-style route triggers and does not verify dragon coins or moons.
- No Starworld files split the No Starworld route, but they do not independently validate rule compliance.

Always test the file before using it for serious attempts.

## How to Download

1. Click the JSON file you want.
2. Click **Raw**.
3. Right-click the raw page.
4. Choose **Save As**.
5. Save the file somewhere easy to find.

Suggested folder:

```text
Documents/Speedrunning/SMW Speedrun/
```

## How to Use

1. Open LiveSplit.
2. Make sure your FXPAK Pro and USB2SNES/QUsb2SNES connection are running.
3. Make sure LiveSplit has the USB2SNES component installed, such as `livesplit-usb2snes.dll`.
4. Load the JSON file for your category.
5. Confirm LiveSplit is reading game memory.
6. Run a short test before doing attempts.

## Testing Checklist

Before trusting a file, check:

- The timer starts at the correct time.
- Normal exits split correctly.
- Keyhole exits split correctly.
- Boss exits split correctly.
- Star World exits split separately when expected.
- The final split ends correctly.
- A wrong exit or route mistake does not cause confusing split behavior.

## Common Problems

### The Timer Does Not Start

Check that the autosplitter is connected, the correct JSON is loaded, and the game memory is being read correctly.

### A Split Happens Too Early Or Too Late

The route may need a different memory condition, or the split may be using a trigger that fires at a different part of the exit animation than expected.

### A Secret Exit Does Not Split

For keyholes, this repo currently uses `1434 > 0`. If a specific secret exit behaves differently, that exit may need a special case.

### Two Splits Happen Together

Some SMW exits share level IDs or exit behavior. Route order usually prevents problems, but paired normal/secret exits should always be tested.

## Versions

GitHub keeps the full history of this repository. If you need an older version of a file, open the commit history and download the file from the older commit.

For known-good public checkpoints, use GitHub releases.

## Credits

Maintained by Mulkey Studios / CookieGames1991.

Built for the Super Mario World speedrunning community.
