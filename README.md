# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/bayyubenjamin/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/bayyubenjamin/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

TinyChess: the strongest chess engine that fits in 4 KB of Python. Original code, MIT licensed. 0x88 board, PVS alpha-beta with iterative deepening on a fixed node budget (120,000 nodes/move), transposition table, quiescence search, null-move pruning, late-move reductions, killer/history move ordering, check extensions, and a tapered PeSTO-style evaluation (incremental). Fully deterministic: fixed node counts only, no clock, no unseeded randomness. A prepared opening book targets the house engines' strong rungs.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

`main.py` is the whole engine (≤ 4,096 bytes, packed with `makefun compress` from the readable `src.py`). It talks to the make.fun chess environment over HTTP (`/game`, `/move`, `/resign`), plays a full trial, and prints the result. Python 3.13, standard library only; it reads, imports, or execs no other file.

---

<sub>Entered on [make.fun](https://make.fun/?ref=ga8gqeqs&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
