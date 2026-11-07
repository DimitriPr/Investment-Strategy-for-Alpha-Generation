# Investment Strategy for Alpha Generation

Replication code for the Applied Investments project. Monthly CRSP x Compustat panel, factor construction (value, profitability, momentum), Fama-French diagnostics, and Gibbs effective spreads.

## Setup

1. Download the data bundle from the [latest Release](../../releases/latest) and unzip it **inside this folder** (next to the notebook). You should end up with:
   ```
   code applied investments.ipynb
   requirements.txt
   CRSP3.csv
   Computstat.csv
   F-F_Research_Data_Factors.csv
   F-F_Research_Data_5_Factors_2x3.csv
   F-F_Momentum_Factor.csv
   crspgibbs.csv
   ```
2. Open the folder in VS Code.
3. Open the notebook, select a Python 3.11+ kernel.
4. Run All. The first cell auto-installs any missing dependencies from `requirements.txt`.

## Data sources

- **CRSP3.csv** - CRSP monthly stock file (PERMNO, MthCalDt, MthRet, etc.), WRDS.
- **Computstat.csv** - Compustat fundamentals annual, WRDS.
- **F-F_\*.csv** - Fama-French 3-factor, 5-factor, and momentum factors (Kenneth French's data library).
- **crspgibbs.csv** - Hasbrouck Gibbs effective half-spreads by (PERMNO, year).

The raw WRDS data cannot be redistributed publicly, which is why this repo is private.

## Requirements

Python 3.11+ with: pandas, numpy, matplotlib, statsmodels, jinja2, ipykernel. See `requirements.txt`.
