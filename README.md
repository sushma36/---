# Box Office Analytics: A Python-Powered Movie Correlation Study

## Overview

This project performs an exploratory data analysis (EDA) and correlation study on a dataset of movies (`movies.csv`) to identify key factors associated with higher gross box office revenue. It utilizes Python libraries like Pandas, NumPy, Matplotlib, and Seaborn for data cleaning, visualization, and statistical analysis to uncover relationships between various movie attributes such as budget, audience votes, genre, company, and more.

## Key Objectives & Features

*   **Data Loading & Preprocessing:** Loaded the `movies.csv` dataset and performed essential cleaning steps, including handling missing values (imputing budget/gross), converting data types, and dropping duplicates.
*   **Feature Engineering:** Created a corrected year column (`yearcorrect`) by extracting information from the `released` date string for more accurate temporal analysis.
*   **Exploratory Data Analysis (EDA):** Investigated initial relationships using visualizations like scatter plots (e.g., Budget vs. Gross) and regression plots via Matplotlib and Seaborn.
*   **Comprehensive Correlation Analysis:** Calculated the Pearson correlation matrix across all relevant features after converting categorical data (genre, rating, company, star, etc.) into numerical representations using Pandas category codes.
*   **Visualization:** Generated correlation heatmaps using Seaborn to provide a clear visual summary of feature interdependencies.
*   **Key Insight Identification:** Identified and ranked the features showing the strongest correlation with gross box office revenue.

## Data Source

The analysis is performed on the `movies.csv` dataset.

*(**Note:** Please ensure this file is included in the repository or provide a link/source if it's publicly available, e.g., from Kaggle. If it's included, you might remove this note).*

## Analysis Steps

1.  **Import Libraries:** Necessary Python libraries (Pandas, NumPy, Seaborn, Matplotlib) are imported.
2.  **Load Data:** The `movies.csv` dataset is loaded into a Pandas DataFrame.
3.  **Data Cleaning:**
    *   Missing values in `budget` and `gross` are imputed with 0 and columns converted to integer type.
    *   Other columns are checked for missing data.
    *   Duplicates are checked (though none were explicitly dropped in the final view shown in the notebook, the code exists).
    *   The `yearcorrect` column is derived from the `released` column.
4.  **EDA & Visualization:**
    *   Initial data structure and types are examined.
    *   Scatter and regression plots are used to visualize the relationship between `budget` and `gross`.
5.  **Correlation Calculation:**
    *   Categorical columns are converted to numerical codes.
    *   Pearson correlation matrix is computed for all features.
    *   A heatmap visualizes the correlation matrix.
    *   Correlation pairs are unstacked and sorted to identify strong relationships.

## Key Findings

*   **Strongest Correlations with Gross Revenue:**
    *   **Budget:** Shows a significant positive correlation (approx. 0.69) with gross earnings, indicating higher budget films tend to gross more.
    *   **Votes:** Audience votes also exhibit a strong positive correlation (approx. 0.57) with gross earnings, suggesting popular films (as measured by votes) achieve higher revenue.
*   **Other Notable Correlations:**
    *   `Votes` and `Budget` have a moderate positive correlation (approx. 0.49).
    *   `Score` shows a moderate positive correlation with `Votes` (approx. 0.41) and `Runtime` (approx. 0.40), but a weaker correlation with `Gross` (approx. 0.17).
*   **Lower Correlations:**
    *   Features like `Company`, `Rating`, `Genre`, `Star`, `Director`, and `Writer` showed lower direct correlations with `Gross` revenue in this specific analysis, *after numerical encoding*. Budget and Votes appear to be stronger indicators in this dataset.

## Technologies Used

*   Python 3
*   Pandas
*   NumPy
*   Seaborn
*   Matplotlib
*   Jupyter Notebook

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    ```
2.  **Navigate to the directory:**
    ```bash
    cd <repository-name>
    ```
3.  **Install required libraries:**
    ```bash
    pip install pandas numpy seaborn matplotlib jupyter
    ```
4.  **Ensure Data File:** Make sure the `movies.csv` file is present in the same directory as the notebook, or update the file path in the first code cell (`pd.read_csv(...)`).
5.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
6.  Open and run the `Movie_correlation.ipynb` notebook cell by cell.
