# Netflix Data Cleaning

A practical data-cleaning exercise using Python, Pandas, and Jupyter
Notebook in VS Code.

## Dataset

Source: https://www.kaggle.com/datasets/shivamb/netflix-shows

The original dataset contains 8,807 rows and 12 columns.

## Cleaning Performed

- Inspected records, data types, statistics, and missing values.
- Corrected three durations incorrectly stored in the rating column.
- Retained unknown director, cast, country, rating, and date values
  as missing rather than guessing.
- Converted date_added from text to datetime.
- Split duration into duration_value and duration_unit.
- Converted duration_value to integers.
- Standardised Season and Seasons to season.
- Checked for exact duplicate rows; none were found.
- Exported the cleaned dataset with 8,807 rows and 14 columns.

## Files

- netflix_cleaning.ipynb: Cleaning steps, explanations, and outputs.
- netflix_titles_cleaned.csv: Cleaned dataset.
- README.md: Project overview.

## How to Run

1. Download netflix_titles.csv from the Kaggle link above.
2. Place it in the same folder as the notebook.
3. Install pandas and ipykernel using:
   `python -m pip install pandas ipykernel`
4. Open the notebook in VS Code with the Python and Jupyter extensions.
5. Select your Python kernel and run the cells from top to bottom.

## Missing-Value Decisions

Missing information was retained when no reliable replacement was
available. Those records still contain useful information for other
analyses.

Minutes and seasons remain separate units and should not be averaged
together. CSV files do not preserve datetime types, so date_added
must be parsed again when reloading the exported file.

## What I Learned

Data cleaning involves understanding problems, making justified
decisions, and verifying changes—not simply deleting every row
with missing information.