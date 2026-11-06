# 🐹 仓鼠种子弹珠 · Hamster Seed Pinball

A pachinko-style mini game powered by a **real hamster**. Drop sunflower seeds onto a
pinball board of acorn pegs, carrot windmill spinners and a big running wheel — the
wheel spins at the **live RPM of Squeektoshi**, the real hamster behind
[Squeekchain](https://squeekchain.com), streamed from the public Squeekchain API.

一款由**真仓鼠**驱动的弹珠小游戏：投下葵花籽，穿过橡子钉阵和胡萝卜风车，落进粮仓格得分。
盘面正中的跑轮转速 = Squeekchain 真仓鼠 Squeektoshi 此刻的真实转速（公开 API 实时数据）。

## Play / 试玩

- **Live:** https://chilperbf24.github.io/hamster-seed-pinball/
- Or just open `index.html` in any browser — single file, no build step, no dependencies.

## Features / 玩法

- 🎡 **Live hamster wheel** — wheel speed, run/sleep state, distance and block progress
  come from `api.squeekchain.com/v1/status` (polled every 5 s). When the hamster runs,
  the wheel flings seeds and the center bin doubles; when it sleeps, night mode slows
  gravity and adds +10% to bin scores. A settled on-chain round during play grants a
  free golden seed.
- 🗺️ **3 boards** — Woodchip Meadow （木屑原野）, Sunflower Valley （瓜子山谷）, Moonlit
  Granary （月夜粮仓）, one featured daily, seeded by date + live block height.
- ⚖️ **Risk & reward** — moldy "stinky corners" (-20), a patrolling beetle that steals
  seeds (-10), combo and harvest-light multipliers.
- ⬆️ **Progression** — earn golden seeds （金瓜子） and EXP each run, level up the hamster
  (scarf → sunglasses → bell → crown), buy upgrades: bigger cheek pouches, richer bins,
  more frequent golden seeds, anti-beetle spray.
- 🏆 **Local leaderboard** — top scores on this device, tagged with map, mode and wallet.
- 👛 **Wallet (Sepolia testnet)** — connect an EVM wallet: saves and leaderboard bind to
  your address, the card shows your SQK balance / Squeeks / power / claimable SQK, and
  the one-click "chain check-in" sends `approve(self, 0)` to the SQK contract
  (0x6872bfa5ccc3e9e440c6c16e5ffdabb8dba4cc76) — the same kind of transaction Genesis
  counts for The Tester badge. Guest play works without a wallet.

## Tech / 技术

Single-file HTML + Canvas + hand-rolled physics. No framework, no build, no tracking.
Game state lives in `localStorage`, keyed per wallet address.

## Disclaimer / 声明

Community prototype built for the Squeekchain Genesis Code program. Not affiliated with
or endorsed by the Squeekchain team. No betting, no token sales, scores cannot be
exchanged for anything. Sepolia testnet only — test assets have no value.
