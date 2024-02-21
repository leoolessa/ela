# Exploratory Data Analysis (EDA) Readme

## Overview

This Python script performs an Exploratory Data Analysis (EDA) on a dataset related to orders from Fake partners in the delivery app. Fake partners represent stores not directly integrated with the app, and the analysis focuses on understanding the price fluctuation of past orders. The goal is to assess the risk of transitioning from a charge-on-delivery to an authorize-and-capture model.

## Code Structure

The analysis is conducted using Python and various libraries such as Pandas, NumPy, Matplotlib, and Seaborn. The code is organized into sections:

1. **Loading and Inspecting the Dataset**
   - The dataset (`orders.csv`) is loaded into a Pandas DataFrame.
   - Basic information, descriptive statistics, and the initial rows of the dataset are displayed.

2. **Data Preprocessing**
   - A new DataFrame (`new_orders`) is created to structure and filter relevant columns from the original dataset.
   - The data is then exported to a new CSV file (`new_orders.csv`).

3. **Authorization Functions**
   - Two functions (`authorized_order` and `incremental`) are defined to determine whether an order is authorized or would be correctly authorized with incremental authorization (+20%).

4. **Authorization Analysis**
   - The authorization status is determined for each order, and the impact of incremental authorization is simulated.
   - The original and simulated percentages of correctly authorized orders are displayed.

5. **Remaining Values Calculation**
   - Values necessary to capture the remaining amount for orders outside of incremental authorization are calculated.

6. **Store Analysis**
   - Statistics related to problematic stores are computed, including the count of under-authorized orders, percentage of under-authorized orders, and monetary value difference.

7. **Correlation Analysis**
   - For under-authorized orders, a correlation analysis is performed between the difference in prices and the likelihood of order cancellation.

## Usage

1. **Requirements**
   - Ensure you have Python installed, along with the required libraries (Pandas, NumPy, Matplotlib, Seaborn).

2. **Dataset**
   - Place the dataset (`orders.csv`) in the same directory as the script.

3. **Execution**
   - Run the script in a Python environment.

## Results and Interpretations

The analysis provides insights into the percentage of under-authorized orders, the impact of incremental authorization, country-wise differences, values necessary for capturing remaining amounts, problematic stores, and correlations between price differences and order cancellations.

## Conclusion

This EDA process aims to assist in the decision-making process for transitioning to an authorize-and-capture model, providing valuable insights into past order patterns and potential risks.

## Notes

- The script assumes a specific dataset structure, and adjustments may be required based on the actual dataset.
- The analysis uses simulated scenarios, and thresholds can be adjusted as needed for incremental authorization.
- Visualization is included for correlation analysis.

Feel free to reach out for any further clarification or customization.