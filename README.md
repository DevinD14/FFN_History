# FFN_History

## Overview
This repository contains a Jupyter notebook `FFN_History_Analysis.ipynb` that conducts a comprehensive analysis of historical data from the Fantasy Football Nation (FFN) universe, focusing on participant trends and performance metrics across various contests. By employing advanced statistical methods and data cleansing, the notebook aims to compute new statistical metrics to account for various biasing factors within the dataset which are then normalized for interepretation.

## Contents
- **Import and Clean Data**: Initial data import and cleaning to prepare datasets for analysis. This step ensures data quality and reliability for subsequent computations.
- **Compute Total Number of Participants in Each Contest**: Calculation of unique participant counts for each league.
- **Compute Adjusted Percentile**: Introduction of a formula to calculate adjusted percentiles, standardizing participant performance across different contest sizes.
- **Data Filtering Options**: Detailed options for filtering the dataset based on various criteria such as time periods, participant demographics, and contest types. This flexibility allows for tailored analyses to uncover specific insights.
- **Summary Statistics**: Provision of summary statistics that offer a snapshot of each player's performance based on the various metrics utilized throughout this analysis.
- **League Performance Index (LPI)**: LPI quantifies a player's Bayesian average adjusted percentile finish. Each player's adjusted percentile finish across all of their league ranking results is computed to account for the variation in the total number of players in a given league. Based on a player's total adjusted percentile finish, the Bayesian average is then calculated to account for the variation in the total number of leagues a given player has participated in.
- **League Performance Index Plus (LPI+)**: LPI+ takes a player's League Performance Index (LPI) and normalizes the number across the entire FFN universe. It then adjusts so a score of 100 is league average, and 150 is 50 percent better than the league average.
- **Data Visualization of League Performance Index Plus (LPI+)**: This bar chart illustrates the comparison of players' performance against the average, marked by a red dashed line at LPI+ 100, visually representing each player's performance deviation above or below the average within the FFN universe.

## Adjusted Percentile Formula
The Adjusted Percentile is calculated using the formula:
$$\text{Adjusted Percentile} = \left( \frac{n - \text{rank}}{n - 1} \right) \cdot \ln(1 + n)$$
where:

- $\text{rank}$ is the position of an individual within the league, with 1 being the highest position.
- $n$ is the total number of participants in the league.
This normalization ensures that performances are comparable across contests with varying degrees of number of participants.

## Bayesian Average and Normalization
The Bayesian Average is utilized to compute new performance metrics, offering a more nuanced view of participant success that accounts for both the number and quality of performances. This method reduces the impact of outliers, providing a more accurate representation of participant capabilities. Metrics are normalized on a scale where 100 signifies average performance, allowing for intuitive comparison across player performance.

## League Performance Index Plus (LPI+) Visualization
This bar chart illustrates the comparison of players' performance against the average, marked by a red dashed line at LPI+ 100, visually representing each player's performance deviation above or below the average within the FFN universe. This plots details the most updated results and provides an overall standings across the FFN universe.

![FFN_universe_lpi_plus_plot](https://github.com/DevinD14/FFN_History/assets/66424619/e743b6d1-2d3b-4a5d-9a57-21faac87bad7)

## Requirements
- Python 3.x
- Jupyter Notebook or JupyterLab
- Required Libraries: `pandas`, `numpy`, `matplotlib`

## How to Run
1. Ensure the installation of Jupyter Notebook and the necessary Python libraries.
2. Download or clone the notebook.
3. Open and execute the notebook cells sequentially to replicate the analysis.
