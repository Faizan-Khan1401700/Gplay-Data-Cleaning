# Google Play Store Dataset Cleaning Project

This repository contains a Python project for cleaning and preprocessing the `gplay.csv` dataset using pandas and numpy. The dataset comprises app details from the Google Play Store, including attributes like app name, category, rating, and installation metrics.

## Dataset Overview

The `gplay.csv` dataset has the following structure:
- **Number of Records**: 10,841
- **Columns**:
  - `App`: Name of the app.
  - `Category`: App category (e.g., ART_AND_DESIGN, GAME).
  - `Rating`: User rating (float, may contain missing values).
  - `Reviews`: Number of reviews (string).
  - `Size`: App size (string with units like M or k).
  - `Installs`: Number of installations (string with commas and "+" symbols).
  - `Type`: Type of app (Free or Paid).
  - `Price`: Price of the app (string, includes "$" for paid apps).
  - `Content Rating`: Target age group for the app.

## Notebook Highlights

The Jupyter Notebook `Python_Project.ipynb` outlines the following steps:

1. **Importing Libraries**:
    - Libraries like `pandas` and `numpy` are used for data manipulation.
    - Warnings are suppressed for a cleaner output.

2. **Loading the Dataset**:
    - The dataset is loaded using `pandas.read_csv()`.

3. **Exploratory Data Analysis (EDA)**:
    - Display dataset information (e.g., shape, column data types).
    - Identify and handle missing values:
        - `Rating` has significant missing values.
        - `Type` and `Content Rating` have minor missing values.
    - Review column data types:
        - `Reviews`, `Size`, `Installs`, and `Price` need conversion from strings to numeric types.

4. **Data Cleaning Steps**:
    - Dropping irrelevant columns (e.g., `Unnamed: 0`).
    - Handling missing values through imputation or removal.
    - Transforming columns:
        - Convert `Reviews` to integer.
        - Normalize `Size` to consistent numeric units (e.g., MB).
        - Remove symbols (`+`, `,`, `$`) from `Installs` and `Price` for numeric conversion.

## Usage Instructions

1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install dependencies:
    ```bash
    pip install pandas numpy
    ```

3. Run the notebook:
    - Open `Python_Project.ipynb` in Jupyter Notebook or JupyterLab.
    - Execute the cells sequentially to perform data cleaning.

4. Analyze the cleaned dataset:
    - Post-cleaning, use the DataFrame for visualization or machine learning tasks.

## Future Scope

- Extend the notebook to include visualizations (e.g., distribution of ratings, installs by category).
- Build a dashboard for interactive data exploration.
