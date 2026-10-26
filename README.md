# Investigating Netflix Movies

## Project Overview

This project is a data exploration and descriptive analytics study of the Netflix movie catalog. The primary goal is to understand how movie characteristics—especially runtime and release year—vary across the catalog, with a focus on comparing movies from the 1990s and later periods. The analysis is performed in a Jupyter Notebook using Python, pandas, and matplotlib, and it follows an exploratory data analysis (EDA) workflow rather than a supervised machine learning pipeline.

The notebook investigates questions such as:

- How long are Netflix movies, on average?
- Do movies from the 1990s differ in runtime from later releases?
- Are specific genres, such as Action, skewed toward shorter durations?
- What patterns emerge when the dataset is filtered and visualized by year and genre?

## Dataset Summary

### Data source

The repository includes the primary dataset file:

- `netflix_data.csv` — a Netflix catalog dataset containing movie metadata.

It also includes a supplemental file:

- `schools.csv` — a secondary dataset present in the repository for additional exploratory work and context.

### Key features

From the Netflix catalog, the notebook uses fields such as:

- `show_id`
- `type`
- `title`
- `director`
- `cast`
- `country`
- `date_added`
- `release_year`
- `duration`
- `description`
- `genre`

These fields allow for filtering by movie type, year range, and genre, and support runtime-based comparisons over time.

### Data preprocessing and cleaning

The notebook performs a straightforward EDA preprocessing workflow:

- Reads the CSV into a pandas DataFrame.
- Filters the dataset to `type == "Movie"`.
- Creates year-based subsets such as movies from the 1990s and 2000s.
- Uses genre-based filtering for targeted analysis (for example, `Action`).
- Converts and validates runtime-related values for comparison.
- Removes or handles missing values where required for clean summaries and visualizations.

This is a classic exploratory analysis pipeline focused on understanding dataset structure, distributions, and trends rather than building a predictive model.

## Project Structure

```text
.
├── README.md
├── .gitattributes
├── notebook.ipynb
├── netflix_data.csv
├── schools.csv
├── redpopcorn.jpg
├── schoolbus.jpg
└── LICENSE (if added in future)
```

The current project is notebook-driven, with the main analysis housed in `notebook.ipynb`. The CSV files contain the raw data used for the visualizations and summaries, while the `.jpg` files are image assets referenced in the notebook.

## Environment & Dependencies

This project is designed for a standard Python data science environment.

### Option 1: pip

```bash
python -m venv .venv
source .venv/bin/activate    # On Windows: .venv\Scripts\activate
pip install --upgrade pip
pip install pandas matplotlib numpy jupyter scikit-learn
```

### Option 2: conda

```bash
conda create -n netflix-eda python=3.10
conda activate netflix-eda
conda install pandas matplotlib numpy jupyter scikit-learn
```

### Recommended packages

- `pandas` — data loading, filtering, and transformation
- `matplotlib` — plotting and exploratory visuals
- `numpy` — numerical operations
- `jupyter` — notebook execution
- `scikit-learn` — optional if you extend the project into modeling workflows

## Notebook Execution Guide

Because this repository currently contains a single notebook, the execution flow is simple:

1. Open the project directory in your terminal or notebook environment.
2. Start Jupyter:

   ```bash
   jupyter notebook
   ```

3. Open `notebook.ipynb`.
4. Run the notebook cells from top to bottom in sequence.
5. Review the exploratory plots and summary outputs after each section.

If the project is expanded in the future, the recommended workflow would be:

```text
01_eda.ipynb -> 02_feature_analysis.ipynb -> 03_modeling.ipynb
```

For the current repository state, the existing notebook effectively covers the full EDA workflow in one place.

## Key Findings & Results

This project is primarily an exploratory analysis, so the results are best interpreted as descriptive insights rather than model performance metrics.

### Main insights

- The notebook compares movie runtime distributions across release-year groups.
- It highlights how movie durations vary with time, especially when isolating the 1990s release window.
- Genre-based filtering reveals runtime patterns within categories such as Action movies.
- The project demonstrates a structured EDA approach: data loading, filtering, summarization, and visual interpretation.

### Notable result pattern

The notebook includes a runtime-based comparison in which action movies from the 1990s are evaluated for shorter film lengths, with explicit counting of movies under a defined threshold (for example, under 90 minutes). This kind of summary supports the project's core conclusion that runtime patterns differ by release period and genre.

### Metrics and reporting

Because this repository does not currently implement a supervised learning model, there are no formal accuracy, RMSE, precision, or recall metrics to report. The output is instead a set of exploratory findings and visual evidence that describe the movie catalog trends.

## Summary

This repository is a compact, notebook-based data science project focused on Netflix movie analysis. It demonstrates an end-to-end EDA workflow using pandas and matplotlib, highlights useful pattern discovery in movie duration data, and provides a clean foundation for future extensions such as predictive modeling, recommendation analysis, or richer visualization dashboards.

For future work, the project could evolve into a more robust modeling exercise by adding features such as:

- user rating prediction,
- genre classification,
- release-year forecasting,
- content recommendation analysis.

