# pandas & Data Visualization — 6 × 2h

For a learner who already knows Python basics (session 0 refreshes them). Each session folder has one `lesson.ipynb`: explanations, code, exercises with solutions, and practice. It works for live teaching and for self-study.

| # | Folder | Dataset | Topics |
|---|---|---|---|
| 0 | `session0_python_basics` | — | types, f-strings, comparisons, lists/slicing, dicts, `if`/`for`, comprehensions, functions, `lambda`, imports, methods vs. attributes |
| 1 | `session1_pandas_basics` | Titanic | DataFrame/Series, `head/info/describe`, `loc/iloc`, filtering, sorting, `value_counts` |
| 2 | `session2_cleaning` | Titanic | missing values, rename/types/drop, new columns, `pd.cut`, `groupby`/`agg` |
| 3 | `session3_first_charts` | Titanic | figure/axes, `df.plot`, seaborn hist/count/bar/box, subplots, `savefig` |
| 4 | `session4_gapminder` | Gapminder | line charts, scatter with hue/size, log scale, `relplot`, annotations |
| 5 | `session5_plotly_project` | Gapminder + choice | plotly express (animated scatter, map), mini-project, next steps |

## Setup

**In the browser (nothing to install):** go to <https://colab.research.google.com> and either **New notebook** to type along, or **Upload** a `lesson.ipynb`.

**On your computer:**

```sh
uv sync
```

Then set your editor's interpreter (e.g. PyCharm) to `.venv/bin/python` and open any `lesson.ipynb`. The project is pinned to uv-managed Python because the python.org build on macOS can lack SSL certificates, which breaks `sns.load_dataset`.

After editing a lesson, check that every notebook still runs from top to bottom:

```sh
uv run jupyter execute session*/lesson.ipynb
```

This does not change the notebooks; it only leaves the files the lessons save (`.png`, `.csv`, `.html`) in the session folders.
