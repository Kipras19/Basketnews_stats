# Euroleague Player Statistics Analysis

This program retrieves a Euroleague basketball player’s **last 10 games statistics** from the BasketNews website and provides interactive analysis, visualizations, and automatic statistical interpretation.

The application is fully terminal-based and allows the user to explore player performance game-by-game or in aggregate form.

---

## Features

### 1) Player Search
The user can enter:
- a **direct Euroleague BasketNews player profile URL**, or
- a **player name / surname** (e.g. `Mike James`)

If a name is entered, the program automatically finds the correct BasketNews profile.

---

### 2) Game-by-Game Analysis
The program displays the **last 10 games** including:
- opponent
- date

The user can then:
- select a specific game,
- choose a statistic (PTS, REB, AST, EFF, etc.),
- view the selected statistic **against that opponent**.

---

### 3) Averages & Statistical Interpretation
For any selected statistic, the program can:
- calculate the **average over the last 10 games**,
- display an **automatic interpretation** based on:
  - **Coefficient of Variation (CV)**
  - **Range (MAX − MIN)**
- optionally display **MIN and MAX values**, including:
  - opponent
  - date of the game

Interpretation is adjusted for:
- counting statistics (PTS, REB, AST, etc.)
- percentage-based statistics (2P %, 3P %, FT %)

---

### 4) Visualizations
The program supports the following chart types:
- Line chart
- Bar chart
- Scatter plot

Additional visualization features:
- custom legend position (top-left, top-right, bottom-left, bottom-right),
- plotting **multiple statistics on the same chart** (e.g. `PTS, REB, FT M/A`),
- dual Y-axes when mixing percentage and non-percentage statistics.

---

### 5) File Export
The user can choose to:
- save the last 10 games data as **CSV**,
- save charts as **PNG**,
- generate a **report folder** containing a `report.txt` file with:
  - player name and profile URL,
  - last 10 games table,
  - all viewed statistics,
  - averages,
  - interpretations (CV + Range),
  - MIN/MAX results,
  - list of saved charts.

---

## Requirements

- Libraries:
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - `matplotlib`

---

## Installation

1. Clone or download the project into a folder.
2. (Recommended) Create a virtual environment:

```bash
python -m venv .venv
3. Activate it (Windows PowerShell)
.\.venv\Scripts\Activate.ps1
4. From the project directory, run:
py main.py
