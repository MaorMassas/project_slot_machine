# 🎰 Slot Machine CLI Game

A lightweight, self‑contained slot machine written in **Python 3.11+**. Play from your terminal, place bets, and chase the 🍒 jackpot—all in less than 200 lines of code.

## Key Features

* **Simple CLI interface** – no external dependencies.
* **Configurable reels** – adjust symbol distribution and payouts in one dictionary.
* **Multi‑line betting** – wager on up to 3 horizontal lines simultaneously.
* **Balance management** – deposit, bet, spin, and cash out.
* **Deterministic testing mode** – set a seed via `--seed` to reproduce spins.

## Installation

```bash
git clone https://github.com/MaorMassas/project_slot_machine.git
cd project_slot_machine
python -m venv .venv && source .venv/bin/activate  # optional
python main.py
```

## How to Play

1. **Deposit** – enter how much money you want in the machine.
2. **Choose lines** – pick 1‑3 lines to wager on (more lines = higher stake).
3. **Set bet per line** – must be between \$1 and \$100 (editable in `constants.py`).
4. **Spin** – hit *Enter* and watch the 3×3 grid populate.
5. **Payout** – matching rows pay according to the table below.

| Symbol | Count on Reels | Payout Multiplier |
| ------ | -------------- | ----------------- |
| A      | 2              | ×5                |
| B      | 4              | ×4                |
| C      | 6              | ×3                |
| D      | 8              | ×2                |

## Example Session

```text
$ python main.py
What would you like to deposit? $100
Enter the number of lines to bet on (1-3)? 3
What would you like to bet on each line? $5
You are betting  $5 on 3 lines. Total bet is equal to: $15

D | A | B
C | A | C
B | A | D

You won $25
You won on lines: 2
Current balance is $110
```

## Configuration

Edit `constants.py` (or the dictionaries at the top of `main.py`) to tweak:

* `MAX_LINE`, `ROWS`, `COLS`
* `symbol_count` – frequency of each symbol
* `symbol_value` – payout multipliers
* betting limits

## Roadmap

* Add diagonal and V‑shape win conditions
* Implement persistent high‑score leaderboard
* Optional GUI with `pygame`
* GitHub Actions CI + unit tests

## Contributing

Pull requests are welcome! Feel free to open issues for bug reports or feature ideas.

## License

[MIT](LICENSE) © 2025 Maor Massas
