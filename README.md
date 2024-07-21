# Immigration Interest Study (2019-2024)

This repository contains the analysis and report on global interest in immigration, based on Google search data from 2019 to 2024.

## Contents

- `Immigration_Interest_Analysis_2019-2024.ipynb`: The Jupyter Notebook containing the data analysis.
- `keywords/`: Directory containing the keyword search data.
- `images/`: Directory containing images used in the report.

## Description

The objective of this study is to identify countries where people are searching for immigration-related keywords in proportion to their population. The analysis includes data processing, normalization, and visualization steps to highlight trends over a five-year period.

## Keywords Selection

The following keywords were selected to capture various aspects of immigration interest:
- Immigration
- Emigrate
- Immigrate
- Migrate
- Move abroad
- Relocation
- Visa application
- Work permit
- Citizenship
- Asylum
- Refugee
- Permanent residency
- Green card
- Border crossing
- Foreign worker
- Expatriate

## Data Collection

Google Trends was used to collect data for each keyword over the five-year period. Each keyword's search interest data was downloaded as CSV files, one file per keyword, covering the period from July 21, 2019, to July 21, 2024.

## Data Processing

The data processing steps are as follows:

1. **Loading and Aggregating Data**: Population data for various countries was loaded from a CSV file. Each keyword CSV file was cleaned and loaded. The keyword data from different years were aggregated to ensure a comprehensive dataset.
2. **Merging Data**: All keyword data was merged on the `Country` column to align keyword search counts with population data. The merged DataFrame was then used to normalize keyword values by population.
3. **Normalization**: For each keyword, the search count was divided by the corresponding country's population to calculate a per capita value, allowing for fair comparisons between countries with different population sizes.
4. **Calculation of Total Interest**: The per capita values for all keywords were summed for each country to obtain a `Total_per_capita` score, representing the overall interest in immigration-related keywords for each country, normalized by population size.

## Visualization

The data was visualized using several plots to make the results more interpretable:

1. **World Map**: A world map was plotted with countries colored based on their `Normalized_Score`, providing a global view of immigration interest.
2. **Bar Chart**: A bar chart was created to highlight the top 10 countries with the highest `Normalized_Score`.
3. **Pie Chart**: A pie chart was plotted to show the proportion of interest in immigration among the top 10 countries.

## How to Use

1. **Clone the repository**:
   ```bash
   git clone https://github.com/aris-barsekhian/Immigration_Interest_Study_2019-2024.git
