# CISC7204 Assignment 02 - Data Visualization with Python

**ZHOU ZHIFAN** (MC651611) | **YOU YUQI** (MC65223)

University of Macau, CISC7204 Data Science and Data Visualization (2026-1, Class L).

## What this repository contains

Completed lab artefacts for the five modules of Assignment 02, the screenshots
used in the personal forums, the revised pair project proposal, and the
complete work package completed by the other Pair 07 member.

### Partner work - YOU YUQI (MC65223)

The complete partner work package is stored under:

| Path | Contents |
|---|---|
| `Partner-YOU-YUQI-MC65223/Module03/` | Module 03 Lab 01 and Lab 02 notebooks with their supporting data and Folium output |
| `Partner-YOU-YUQI-MC65223/Module05-Practice/` | Module 05 Practice Lab 01 notebook and Lab 02 Dash project |
| `Partner-YOU-YUQI-MC65223/Module05-Final/` | Module 05 Final Lab 02 project archive and runnable Dash project |
| `Partner-YOU-YUQI-MC65223/screenshots/` | Executed code and output screenshots grouped by lab |
| `Partner-YOU-YUQI-MC65223/booklets/` | Complete screenshot booklets for Module 03 and Module 05 |
| `Partner-YOU-YUQI-MC65223/README.md` | Partner submission summary and delivery checklist |

### Module 01 - Introduction to Data Visualization

| File | Lab |
|---|---|
| `Module01/CISC7204 Assgn02 Module 01 - Lab01 MC651611 ZHOU ZHIFAN.ipynb` | Exploring and pre-processing a dataset with pandas |
| `Module01/CISC7204 Assgn02 Module 01 - Lab02 MC651611 ZHOU ZHIFAN.ipynb` | Introduction to Matplotlib and line plots |

### Module 02 - Basic and Specialized Visualization Tools

| File | Lab |
|---|---|
| `Module02/...Module 02 - Lab01...ipynb` | Area plots, histograms and bar charts |
| `Module02/...Module 02 - Lab02...ipynb` | Pie charts, box plots, scatter plots and bubble plots |
| `Module02/...Module 02 - Lab03...ipynb` | Plotting directly with Matplotlib |

### Module 03 - Advanced Visualizations and Geospatial Data

| File | Lab |
|---|---|
| `Module03/...Module 03 - Lab01...ipynb` | Waffle charts, word clouds and regression plots |
| `Module03/...Module 03 - Lab02...ipynb` | Creating maps and visualising geospatial data (Folium, choropleth) |

### Module 04 - Creating Dashboards with Plotly and Dash

| File | Lab |
|---|---|
| `Module04/...Module 04 - Lab01...ipynb` | Plotly basics: scatter, line, bar, bubble, histogram, pie, sunburst |
| `Module04/...Module 04 - Lab02...zip` | Dash basics - `dash_basics.py` |
| `Module04/...Module 04 - Lab03...zip` | Add interactivity - `dash_interactivity.py` and `dash_interactivity_barplot.py` |
| `Module04/...Module 04 - Lab04...zip` | Flight delay time statistics dashboard - `flight_delay.py` |

### Module 05 - Practice Project

| File | Lab |
|---|---|
| `Module05-Practice/...Module 05Practice - Lab01...ipynb` | Analysing wildfire activities in Australia |
| `Module05-Practice/...Module 05Practice - Lab02...zip` | Creating dashboards - `dash_layout.py` and `Dash_Auto.py` |

### Module 05 - Final Project

| File | Lab |
|---|---|
| `Module05-Final/...Module 05Final - Lab01...ipynb` | Visualisations with Matplotlib, Seaborn and Folium (Tasks 1.1 - 1.10) |
| `Module05-Final/...Module 05Final - Lab02...zip` | Creating a dashboard with Plotly and Dash |

### Supporting material

| Path | Contents |
|---|---|
| `screenshots/` | Screenshots of each major task (code and executed output), grouped by lab and numbered in notebook order |
| `CISC7204-Assgn02-Pair07-RevisedProjectProposal.docx` | Final revised pair project proposal, 5 A4 pages |

## Running the notebooks

The notebooks read their datasets directly from the IBM Skills Network public
data URLs, so no local data files are needed. They were executed with
Python 3.12, pandas 2.2, matplotlib 3.11, plotly 7, dash 4 and folium 0.20.

The Dash project spaces are zipped together with a short README that lists the
run command for each script:

```
pip install pandas dash plotly
python <script>.py
```

## Notes on code changes

The lab sources were written for an older environment. Where a library removed
or renamed an interface, the code was updated and the change is noted in the
relevant cell:

- `DataFrame.sum(axis=1)` is called with `numeric_only=True` so that the text
  columns are not summed.
- `folium.Map.choropleth(...)` is replaced by `folium.Choropleth(...).add_to(...)`,
  and the Stamen tile aliases are requested from the Stadia Maps endpoints.
- The Dash scripts use `dash.Dash`, `from dash import dcc, html` and
  `app.run(...)`, matching Dash 3/4.
- The JupyterLite-only `fetch` calls are replaced by `pandas.read_csv` and
  `urllib.request` on the same public data URLs.
