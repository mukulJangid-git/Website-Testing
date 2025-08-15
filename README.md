# Website-Testing

Website A/B Testing for Conversion Optimization
📈 Project Overview
This project provides a comprehensive walkthrough of a website A/B test to determine if a new checkout funnel (Variant B) outperforms the old one (Variant A). Using Python and key data science libraries, this notebook simulates click-through and purchase data, calculates conversion rates, and performs statistical tests to arrive at a data-driven conclusion.

The analysis covers both a standard A/B test and a simulation of real-time sequential testing, demonstrating how results are monitored as data is collected over time.

✨ Key Features & Concepts
A/B Test Simulation: Simulates user interaction data (visits vs. purchases) for two website variants using a binomial distribution.

Conversion Rate Analysis: Calculates the observed conversion rates for each variant.

Confidence Intervals: Computes the 95% confidence interval for the conversion rates to quantify uncertainty in the estimates.

Data Visualization: Plots the conversion rates with error bars for a clear visual comparison of performance and statistical overlap.

Hypothesis Testing: Performs a two-proportion z-test to determine if the observed difference in conversion rates is statistically significant.

Real-Time Monitoring: Simulates a sequential A/B test, updating metrics and statistical significance in batches to mimic a live dashboard and highlight the evolution of the p-value and lift over time.

🛠️ Technologies & Libraries Used
Python: The core language for the analysis.

NumPy: For numerical operations and simulating binomial data.

Pandas: For creating and displaying a summary table of the results.

Matplotlib: For plotting the conversion rates and their confidence intervals.

SciPy & Statsmodels: For performing the statistical z-test and calculating confidence intervals.

🚀 How to Run This Project
To get started with this project, you'll need Python and Jupyter Notebook installed on your machine.

Clone the repository:

Bash

git clone <your-repository-url>
Navigate to the project directory:

Bash

cd <your-project-directory>
Install the required libraries:

Bash

pip install numpy pandas matplotlib scipy statsmodels
Run the Jupyter Notebook:

Bash

jupyter notebook Website_testing.ipynb
This will open the notebook in your browser. You can then run the cells sequentially to see the simulation and analysis.

📊 Methodology
The project follows a structured, five-step approach to A/B testing:

1. Simulate Data
We begin by simulating a realistic dataset where each of the two variants (A and B) receives 10,000 visitors.

Variant A (Control): Has a true conversion rate of 10%.

Variant B (Treatment): Has a true conversion rate of 12%.
The actual number of conversions for each group is drawn from a binomial distribution to reflect real-world randomness.

2. Calculate Conversion Rates & Confidence Intervals
We compute the observed conversion rate for each variant and calculate the 95% confidence interval to understand the range in which the true conversion rate likely falls.

3. Plot the Results
A bar chart is generated to visually compare the conversion rates. Error bars representing the 95% confidence intervals are included, providing an intuitive way to see if the performance difference is significant.

4. Perform a Two-Proportion Z-Test
A one-sided z-test is conducted to formally test the hypothesis:

Null Hypothesis (H₀): The conversion rate of B is less than or equal to A (CR_B ≤ CR_A).

Alternative Hypothesis (H₁): The conversion rate of B is greater than A (CR_B > CR_A).

A p-value below 0.05 allows us to reject the null hypothesis, confirming that Variant B is statistically superior.

5. Real-Time Sequential Testing
This final step simulates how an A/B test is monitored in a live environment. Data is processed in batches, and the p-value and lift are recalculated at each step. This demonstrates how statistical confidence evolves over time and highlights the risks of "peeking" at results too early.
