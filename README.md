# ⚽ Advanced Football Match Data Analysis with Python

This project performs **advanced data analysis** on a raw football match dataset. The goal is to extract meaningful insights for any match using historical team performance over the last _n_ games. The core logic is encapsulated in a reusable Python class: `Arpit`.

---

## 📌 Project Highlights

- Written in **Python** using **Pandas**
- Automatically extracts stats for a given match index:
  - Goals scored
  - Shots taken
  - Shots on target
  - Fouls committed
  - Corners won
  - Yellow and red cards
  - Match outcomes: Wins / Losses / Draws
- Works with **raw historical football data**
- Easily configurable number of recent matches (`n`) to consider

---

## 🧠 How It Works

The `Arpit` class:
- Takes in the full match DataFrame and a `match_index` (1-based)
- Analyzes both teams’ performance in their last _n_ matches
- Computes and prints metrics like goals, shots, cards, results, etc.

```python
from analysis import Arpit
import pandas as pd

# Load your football data
df = pd.read_csv('matches.csv')

# Analyze a specific match (e.g., match 50)
model = Arpit(df, match_index=50, n=5)

Match 50: Chelsea vs Arsenal
Chelsea goals in last 5 matches: 7
Arsenal goals in last 5 matches: 10
Chelsea shots in last 5 matches: 65
Arsenal shots in last 5 matches: 58
Chelsea wins in last 5 matches: 3
Arsenal wins in last 5 matches: 4
...
