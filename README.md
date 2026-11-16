# tiny-chess-01

A 4 KB Python chess engine: 0x88 board, alpha-beta with iterative deepening
(depth 5, 90,000-node cap), quiescence search, MVV-LVA move ordering, a
transposition table, and material + piece-square evaluation. No model calls,
no network beyond the trial env, deterministic fixed-node search.

[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Dhaniels033/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Dhaniels033/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

## Run

`MAKEFUN_ENV_URL=<env> python3 main.py` — plays the gauntlet via the env
(`/game`, `/move`, `/resign`).

## Packing

`main.py` is packed from the readable `engine.py` with the kit's
`makefun compress` (`engine.py` stays uncommitted next to it). Verified
strength in practice trials: mean Elo 1,191, above the 1,154 final-entry bar.
