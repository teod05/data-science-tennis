# Tennis Data Science Analysis

This project explores ATP tennis match data to understand patterns in player performance, ranking effects, and match outcomes.

## Data Source

**Data:** [Jeff Sackmann's tennis_atp repository](https://github.com/JeffSackmann/tennis_atp)

**Initial Dataset:** `tennis_atpatp_matches_combined.csv`
- **Rows:** 126,167 matches
- **Columns:** 49 features

## Analyses

### 1. Upset Probability vs ATP Rank Gap

**Question:** How does the probability of an upset (lower-ranked player beats higher-ranked) change with rank difference?

**Key Findings:**
- Higher-ranked players win ~65.4% of matches overall
- Upset probability declines with larger rank gaps
- Small gaps (0-5) yield ~46% upset rate (nearly coin-flip)
- Large gaps (200+) drop to ~23% upset rate

**Notebooks:** `player-rangking.ipynb`, `upset_probability.ipynb`

---

### 2. Ace Rate Differences by Handedness

**Question:** Do left-handed servers produce different ace-rate distributions compared to right-handed servers?

**Key Findings:**
- Left-handed and right-handed players show similar ace rate distributions
- Minor differences observed at the upper tail
- Handedness alone does not dramatically shift ace-rate distribution
- Surface and player style likely matter more

**Notebook:** `handedness_aces.ipynb`

---

### 3. Country Win Rates by Surface

**Question:** Do players from certain countries excel on specific surfaces?

**Key Findings:**
- Top national win rates vary significantly by surface
- Some countries show consistent strengths (e.g., higher on grass or clay)
- National profiles can inform scouting and previewing content
- Individual player effects dominate within nations

**Notebook:** `nationality.ipynb`

---

### 4. What Drives Match Duration?

**Question:** What features correlate with match duration (minutes)?

**Key Findings:**
- Weak negative correlations with first-serve-win% and ace difference
- Relatively weak positive correlation with "pressure" (break points faced)
- Rank gap shows minimal linear relationship with duration
- Match format, set length, and competitiveness likely better predictors

**Notebook:** `feature_to_duration.ipynb`

---

## Project Structure

```
tennis/
├── main/
│   ├── player-rangking.ipynb        # Ranking analysis and upsets
│   ├── upset_probability.ipynb      # Upset probability by rank gap
│   ├── handedness_aces.ipynb        # Handedness vs ace rates
│   ├── nationality.ipynb            # Country performance by surface
│   ├── feature_to_duration.ipynb    # Match duration correlations
│   ├── player_feature.ipynb         # Serve statistics analysis
│   └── sorting_data.ipynb           # Data processing utilities
├── tennis_atp/
│   └── tennis_atpatp_matches_combined.csv  # Main dataset
└── README.md
```

## Requirements

- Python 3
- pandas
- matplotlib
- numpy
- scipy

## Usage

Each analysis is self-contained in its respective Jupyter notebook. Simply open the notebook and run all cells to reproduce the results.

