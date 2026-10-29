# Information Visualization Assignments

Jupyter notebooks for the Information Visualization course assignments, covering
statistical plots, geographic maps, heatmaps, dimensionality reduction, and network layouts
in Python.

## Contents

| Notebook | Topic | What it does |
|---|---|---|
| `notebooks/a1_1_life_expectancy_line_chart.ipynb` | Line charts | Plots mean life expectancy at birth per continent, 1990–2021 |
| `notebooks/a1_2_tasks1-2_maternal_mortality.ipynb` | Distributions & uncertainty | Histogram/KDE of maternal mortality rates across countries (2022); global trend line with confidence band |
| `notebooks/a1_2_task3_pairgrid_scatter.ipynb` | Scatterplot matrix | Seaborn `PairGrid` with regression lines for life expectancy, GDP, BMI and infant deaths (2015) |
| `notebooks/a2_1_tasks1-2_choropleth_heatmap_clustermap.ipynb` | Maps, heatmaps | Diverging-colormap choropleth of European life expectancy, plus a heatmap and clustermap (2005–2021) |
| `notebooks/a2_2_task1_dimensionality_reduction.ipynb` | Dimensionality reduction | PCA (with and without standardization), MDS and t-SNE on health indicators for selected countries |
| `notebooks/a2_2_task2_network_layouts.ipynb` | Graph layouts | Radial, Kamada-Kawai and Fruchterman-Reingold layouts of a network read from an edge list |

The `a1_*` / `a2_*` prefixes refer to assignment 1 and assignment 2 (and their sub-parts).

## Tech stack

Python 3, `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `geopandas`, `scikit-learn`, `networkx` (see `requirements.txt`).

## Repository layout

```
.
├── README.md
├── requirements.txt
├── data/        # CSV inputs (see data/README.md)
└── notebooks/   # one notebook per assignment task
```

## Data

The notebooks read their inputs from `data/` using relative paths (`../data/...`). See
[`data/README.md`](data/README.md) for the file list and sources.

One file is **not** included: the country-boundary GeoJSON `CNTR_RG_20M_2024_3035.geojson`
used by the choropleth notebook. Download it from Eurostat GISCO and put it in `data/`.

## Running

```bash
git clone <this-repo-url>
cd infoviz-assignments
pip install -r requirements.txt
cd notebooks
jupyter notebook
```

Run notebooks from inside `notebooks/` so the relative data paths resolve.

## Notes

- The choropleth notebook contains embedded Plotly output, which is why that file is much larger than the others.
- Course assignments: please don't copy solutions for your own coursework submissions.
