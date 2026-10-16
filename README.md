COVID-19 India: Exploratory Data Analysis (EDA)

A beginner-friendly exploratory data analysis of COVID-19 cases in India, built in Google Colab using Python. The notebook also includes a few introductory statistics and probability exercises.

## Dataset

- Source: [COVID-19 in India](https://www.kaggle.com/datasets/sudalairajkumar/covid19-in-india) on Kaggle (by Sudalai Rajkumar)
- File used: 'covid_19_india.csv' (18,110 rows, 9 columns)
- Period covered: 30 Jan 2020 to 11 Aug 2021
- Key columns: 'Date', 'State/UnionTerritory', 'Cured', 'Deaths', 'Confirmed'

The dataset is downloaded automatically with 'kagglehub'.

What the Notebook Does

1. Data loading and inspection: shape, columns, dtypes, null values, duplicates
2. Cleaning and feature engineering:
   - Converts 'Date' to datetime
   - Creates 'Recovered' and 'Active' (Confirmed - Deaths - Recovered) columns
3. State-level summary: max Confirmed, Deaths, Recovered and Active per state/UT, plus Recovery Rate and Death Rate (%)
4. Visualizations (Matplotlib and Seaborn):
   - Top 10 states by confirmed cases
   - Top 10 states by deaths
   - Top 10 states by recovery rate
   - Line chart of confirmed cases over time

Requirements

- Python 3
- 'pandas', 'numpy', 'matplotlib', 'seaborn', 'kagglehub'

bash
pip install pandas numpy matplotlib seaborn kagglehub

How to Run

1. Open 'COVID-19_EDA_project.ipynb' in Google Colab or Jupyter.
2. Run the cells from top to bottom.
3. Kaggle access may be needed for kagglehub to download the dataset.

Known Issues / Notes

- Some state names appear twice with spelling variants or footnote markers (e.g. Maharashtra***, Karanataka), which inflates the Top 10 charts. Clean these names before grouping.
- The bar charts use a 3-color palette for 10 bars, so colors repeat. Use a single color or a larger palette.
- The last bar-chart cell references a 'Province/State' column that does not exist in this dataset (it should be 'State/UnionTerritory'), so it will raise an error.
- The employee salary example has inconsistent values across cells, since '28' was later edited to 28000'. Re-run the cells in order.

Author

Created as a learning project for exploratory data analysis with Python.
