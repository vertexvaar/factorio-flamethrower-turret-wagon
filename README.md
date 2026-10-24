# Flamethrower Wagon

Factorio 2.1 mod (Space Age optional). A fluid wagon with two flamethrower turrets on its roof. They work like
flamethrower turrets, also while the train is moving, and burn oil from the wagon's tank.

- Fill the wagon with crude oil, heavy oil or light oil (25,000 units). Each flamethrower keeps its tank full.
- The flamethrowers cover all sides, turn and unfold faster than a flamethrower turret and also fire at enemies
  right next to the train (minimum range 2 instead of 6). The wagon itself is immune to fire; other rolling stock
  close to the burning area is not.
- Flamethrower damage research applies as usual. Wagon quality carries over to the flamethrowers.
- Works on elevated rails.
- Unlocked by the technology "Flamethrower wagon" (after fluid wagon and flamethrower).

## How it works

Factorio has no turrets on rolling stock. Each wagon gets two hidden turrets (not selectable, not attackable,
no collision). While the wagon moves, the script teleports them along with it every tick; standing wagons cost
nothing per tick. Every 30 ticks the flamethrowers are topped up from the wagon's tank.
## Tests

    python tests/run.py                 # headless, with Space Age
    python tests/run.py --no-space-age
    python tests/ingame.py              # opens a game window: build, mine, ghost revive, blueprint
    python tests/shots.py               # opens a game window briefly, writes previews/shots/*.png

## Release

    python tools/package.py             # dist/<name>_<version>.zip
    python tools/publish.py publish     # first release (needs FACTORIO_API_KEY)
    python tools/publish.py upload      # later releases
