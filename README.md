# Customer Cohort Analysis Project

## Overview

This project performs customer cohort analysis to understand customer behavior over time. The main goal is to observe how customer engagement evolves over months following their first transaction.

## Project Structure

- `main.ipynb`: Python script containing the cohort analysis functions and example.
- `input`: Folder containing the sample input file.

## Functions

`make_cohort(df: pd.DataFrame) -> pd.DataFrame`

This function performs cohort analysis on the input DataFrame `df`. It calculates the percentage of customers still active after x months from their first transaction and presents the results in a pivoted DataFrame.

`plot_cohort(df_cohort: pd.DataFrame, cmap: str = "RdYlGn") -> None`

This function generates a heatmap plot of the cohort analysis results using the seaborn library. It provides a visual representation of customer retention over time.

`check_cohort(raw_df: pd.DataFrame, cohort_df: pd.DataFrame) -> bool`

This function checks the accuracy of the cohort analysis by comparing the results with manual calculations for the first three months.

`fillna_diagonal_lower_right(df: pd.DataFrame) -> pd.DataFrame`

This utility function fills the lower-right diagonal of the DataFrame with NaN values.

## Usage

To use the cohort analysis functions, follow the steps outlined in the `main.ipynb` notebook. Ensure you have the required dependencies installed, such as pandas, numpy, seaborn, and matplotlib.

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn

## Example

```python
import pandas as pd

# Load your dataset
data = pd.read_csv("your_dataset.csv")

# Perform cohort analysis
cohort_df = make_cohort(data)

# Plot the cohort analysis
plot_cohort(cohort_df)
```