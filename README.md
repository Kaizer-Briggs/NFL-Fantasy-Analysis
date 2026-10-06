# NFL Fantasy Football Analysis

An exploratory data analysis of six NFL seasons of player-week data, testing which statistics actually predict fantasy points and which positions score most consistently.

## The Question

Fantasy players make weekly decisions from raw stats, but which stats really drive fantasy production, and how reliable is each position from week to week?

## Data

- **Source:** [nflverse](https://github.com/nflverse), a public NFL data project
- **Seasons:** 2020–2025
- **Size:** 112,450 player-week records across six seasons
- **After cleaning:** 38,146 fantasy-relevant rows

## Process

1. **Explore:** inspected the raw data, ran descriptive statistics, and visualized distributions
2. **Correlate:** used scatterplots and correlations to relate usage stats (such as targets) to fantasy points
3. **Clean:** removed non-fantasy positions, handled missing values, and screened outliers
4. **Re-analyze:** repeated the statistics and visualizations on the cleaned data
5. **Recommend:** translated findings into draft and start-or-sit guidance

## Key Findings

- **Usage drives production.** Targets are strongly correlated with fantasy points (r ≈ 0.81).
- **Not all "junk" data is junk.** Games where a player had zero targets or carries looked like noise, but removing them *weakened* the targets-to-points correlation from 0.806 to 0.778. A player with no touches scoring near zero is real signal, so those rows were kept. Every cleaning step was tested before it was applied.
- **Quarterbacks are the most consistent position.** Coefficient of variation of 0.67, compared with 1.08 for tight ends.

## View the Analysis

Open [`analysis.ipynb`](analysis.ipynb) to read the full notebook, with code, charts, and written analysis, right here on GitHub. `analysis.html` is the same notebook as a standalone page you can download and open in any browser.

## Run It Yourself

The notebook downloads the data directly from nflverse's public releases, so no data files are needed.

```bash
pip install -r requirements.txt
jupyter notebook analysis.ipynb
```

## Built With

Python, Pandas, NumPy, Matplotlib, Jupyter Notebook

## Author

**Kaizer Briggs** · Data Science, Baylor University
