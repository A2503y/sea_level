# EPA Sea Level Rise Analysis

This project analyzes historical sea level data from the EPA to visualize trends and predict future sea level rise.

## Project Overview

The core of this project is a Jupyter Notebook (`epa_sea_level.ipynb`) that performs the following tasks:

1.  **Data Loading:** Imports sea level data from the `epa-sea-level.csv` file using Pandas.
2.  **Scatter Plot:** Creates a scatter plot of "Year" versus "CSIRO Adjusted Sea Level".
3.  **Linear Regression (All Data):**
    *   Calculates the line of best fit for the entire dataset using `scipy.stats.linregress`.
    *   Plots this line of best fit, extending it to the year 2050.
4.  **Linear Regression (2000 Onwards):**
    *   Calculates a new line of best fit using only data from the year 2000 onwards.
    *   Plots this second line of best fit, also extending it to the year 2050.
5.  **Predictions:**
    *   Predicts the sea level in 2050 based on both regression lines.
    *   Calculates and displays the difference between these two predictions.
    *   Includes a 95% confidence interval for the 2050 prediction based on all data.
6.  **Plot Formatting:**
    *   Adds labels, a title, a legend, and a grid to the plot for clarity.
    *   Includes a vertical line at 2050 for reference.
    *   Annotates the 2050 predictions on the plot.
7.  **Output:**
    *   Displays the generated plot.
    *   Saves the plot as `sea_level_analysis.png`.
    *   Prints various analytical results, including regression statistics and prediction values.

## Files

*   `epa_sea_level.ipynb`: The Jupyter Notebook containing the Python code for the analysis.
*   `epa-sea-level.csv`: (Assumed) The input CSV file containing the sea level data. This file is referenced in the notebook but not included in this repository.
*   `sea_level_analysis.png`: (Generated) The output plot image created by the notebook.
*   `README.md`: This file.

## Requirements

The analysis relies on the following Python libraries:

*   `pandas`: For data manipulation and CSV file handling.
*   `matplotlib`: For creating plots.
*   `numpy`: For numerical operations, particularly for creating extended year ranges.
*   `scipy`: For statistical functions, specifically linear regression (`linregress` and `stats`).

You can typically install these using pip:

```bash
pip install pandas matplotlib numpy scipy
```

## How to Run

1.  **Ensure you have the data:** Make sure the `epa-sea-level.csv` file is in the correct location as referenced by the notebook (currently `C:/Users/Mehak/Downloads/epa-sea-level.csv`). You might need to update this path in the notebook if your file is located elsewhere.
2.  **Open and run the Jupyter Notebook:**
    *   Launch Jupyter Notebook or JupyterLab.
    *   Navigate to the directory containing `epa_sea_level.ipynb`.
    *   Open the notebook.
    *   Run all cells in the notebook.

The notebook will then:
*   Print statistical outputs to the console.
*   Display the sea level rise plot.
*   Save the plot as `sea_level_analysis.png` in the same directory.

## Output Interpretation

The primary output is the `sea_level_analysis.png` plot, which shows:
*   The historical sea level data points.
*   A line of best fit based on all available data, projected to 2050.
*   A second line of best fit based on data from 2000 onwards, also projected to 2050.
*   Annotations indicating the predicted sea level in 2050 from both models.

The console output provides:
*   Details of the linear regression models (slope, intercept, R-squared, p-value).
*   Specific sea level predictions for 2050 from both models.
*   The 95% confidence interval for the 2050 prediction using all data.
*   Other analytical details like the data range and average annual rise.

This information helps in understanding the rate of sea level change and how different timeframes for analysis can affect future predictions.
