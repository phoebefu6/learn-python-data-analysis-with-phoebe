# Official course map - learn-python-data-analysis-with-phoebe

**Course:** Python for Data Analysis, taught as one running project.
**Audience:** KOL followers / self-learners who can write a little Python (sequel to learn-python-with-phoebe). Single builder track.
**Spine:** running-project. One real messy dataset carried load -> clean -> explore -> visualize -> insight -> shareable report across 8 sessions.
**Sessions:** 8 x 45 min (3 welcome / ~15 concepts / ~22 build-along / 5 Q&A).
**By Phoebe Fu.** Palette: Python blue #3776AB / yellow accent.

## The running project - "Decode the Data Job Market"

Dataset: **LinkedIn Job Postings (2023-2024)** by arshkon on Kaggle - <https://www.kaggle.com/datasets/arshkon/linkedin-job-postings>
- 124k+ postings, multi-table: `postings.csv` + `companies/` + `jobs/` (skills, salaries, benefits) + mapping tables.
- Verified messiness: ~70% of postings have missing salary, salaries split across min/max/pay-period columns, messy free-text job titles and skill names, mixed dtypes, duplicate postings. This mess is the teaching material.
- Learner deliverable by Session 8: a shareable "state of the data job market" mini-report (charts + 5 findings + a salary model) fit to post on LinkedIn.
- Fallback if the multi-table version is too heavy for a cohort: `ds_salaries.csv` (Data Science Job Salaries) - single clean table, but too clean to teach cleaning, so used only as a demo-B comparison.

Re-verify before delivery: Kaggle dataset versions change; confirm file names + row count against the dataset page (note dataset last checked 2026-07-18).

## Source universe (the 80% bar)

Each session teaches ~80% of its mapped sources' working content. Certificates, graded exercises, and videos stay on the official platforms - stated honestly on each page. Four source families:

1. **pandas** official User Guide + "10 minutes to pandas" - <https://pandas.pydata.org/docs/user_guide/>
2. **NumPy** fundamentals / absolute beginners - <https://numpy.org/doc/stable/user/absolute_beginners.html>
3. **matplotlib** (pyplot + Artist/Axes) - <https://matplotlib.org/stable/users/> and **seaborn** tutorial - <https://seaborn.pydata.org/tutorial.html>
4. **Kaggle** micro-courses: Pandas, Data Visualization, Intro to Machine Learning - <https://www.kaggle.com/learn>
5. Cross-cutting text: **Wes McKinney, Python for Data Analysis, 3e** (open access) - <https://wesmckinney.com/book/>
6. Profiling libs woven in: **ydata-profiling** (Session 1 first look), **missingno** (Session 4 cleaning), **sweetviz** (self-study).

### Verified source structures (fetched / searched 2026-07-18)

- **Kaggle Pandas** (6 lessons): Creating/Reading/Writing · Indexing, Selecting & Assigning · Summary Functions and Maps · Grouping and Sorting · Data Types and Missing Values · Renaming and Combining.
- **Kaggle Data Visualization** (7): Hello Seaborn · Line Charts · Bar Charts and Heatmaps · Scatter Plots · Distributions · Choosing Plot Types and Custom Styles · Final Project.
- **Kaggle Intro to Machine Learning** (7): How Models Work · Basic Data Exploration · Your First ML Model · Model Validation · Underfitting/Overfitting · Random Forests · ML Competitions.
- **McKinney 3e** (13 ch): 1 Preliminaries · 2 Python/IPython/Jupyter · 3 Built-in Structures/Functions/Files · 4 NumPy Basics · 5 Getting Started with pandas · 6 Data Loading/Storage/Formats · 7 Data Cleaning & Preparation · 8 Data Wrangling: Join/Combine/Reshape · 9 Plotting & Visualization · 10 Data Aggregation & Group Operations · 11 Time Series · 12 Modeling Libraries (statsmodels/scikit-learn) · 13 Data Analysis Examples.

## Per-session coverage (checkeys: ✓ full · ◐ partial/intro)

| # | Session | Sources mapped | Coverage |
|---|---------|----------------|----------|
| 1 | Setup + the mission | Kaggle Pandas L1 · McKinney ch1-2, ch6 (read_csv) · ydata-profiling | ✓ env/Jupyter, load csv, first look, profile report · ◐ pandas IO (more ch6 in S4/S5) |
| 2 | NumPy foundations | NumPy absolute-beginners + fundamentals · McKinney ch4 | ✓ ndarray, dtype, vectorization, broadcasting, ufuncs, boolean/fancy index · ◐ structured arrays (self-study) |
| 3 | pandas core | Kaggle Pandas L1-L3 · pandas 10-min + indexing/selecting · McKinney ch5 | ✓ Series/DataFrame, loc/iloc, boolean filter, assign, summary fns, map/apply · ◐ MultiIndex (intro) |
| 4 | Cleaning messy data | Kaggle Pandas L5 · pandas missing-data + text · McKinney ch7 · missingno · ydata-profiling | ✓ NA patterns (missingno viz), dropna/fillna, dtype coercion, str methods, salary parse, dates, dedupe · ◐ categoricals (intro) |
| 5 | Explore + aggregate | Kaggle Pandas L4, L6 · pandas groupby + merge/join/concat + pivot · McKinney ch8, ch10 | ✓ groupby/agg, pivot_table, merge/join the tables, concat, reshape · ◐ hierarchical index (working level) |
| 6 | Visualization I - matplotlib | matplotlib pyplot + Artist layer · McKinney ch9 | ✓ figure/axes anatomy, line/bar/hist/scatter, subplots, labels/styling, savefig · ◐ animation (not covered) |
| 7 | Visualization II - seaborn | seaborn tutorial · Kaggle Data Viz L1-L6 | ✓ figure- vs axes-level, relplot/displot/catplot, heatmap, correlation, themes, publication polish · ◐ jointplot/pairgrid (self-study) |
| 8 | Insight -> shareable report | Kaggle Intro to ML L1-L4 · McKinney ch12-13 · scikit-learn basics | ✓ train/test split, LinearRegression salary model, validation (MAE/R2), synthesize findings, export report + carousel · ◐ random forests, feature engineering (intro/next-steps) |

## Not covered by design (stated on pages)

- Graded Kaggle exercises, certificates, competition submission - do these on kaggle.com.
- Deep statistics / hypothesis testing (scipy.stats) - out of scope; pointer given.
- Big-data / out-of-core (polars, Dask, Spark) - named as "when pandas stops fitting in RAM", not taught.
- Time-series forecasting (McKinney ch11 depth) - dates covered in S4 only for cleaning.
- ML depth: random forests, cross-validation, pipelines, deployment - S8 is a first honest taste, points to Kaggle Intermediate ML.
- Geospatial mapping of listings - out of scope.

## Honest framing line (goes on each Official-sources section)

"This session teaches the working content of the official pandas / NumPy / matplotlib / seaborn docs, the free Kaggle micro-courses, and Wes McKinney's open-access Python for Data Analysis (3e). Certificates, graded exercises, and videos stay on those platforms - links provided."
