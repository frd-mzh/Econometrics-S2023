# Voting Outcomes and Campaign Expenditures

## Overview
This project investigates the relationship between campaign expenditures and voting outcomes in U.S. elections. The dataset includes variables such as state, district, party affiliation, campaign expenditures, and voting percentages. The goal is to analyze how campaign spending by candidates affects their voting outcomes and to identify any causal relationships.

## Dataset Description
The dataset contains the following variables:
- **State**: Postal code of each state that contributed to the election.
- **District**: The number of each district in every state.
- **democA**: Indicates if the nominee is a Democrat (1) or not (0).
- **voteA**: The percentage of votes received by candidate A.
- **expandA**: Campaign expenditure by candidate A.
- **expandB**: Campaign expenditure by candidate B.
- **prtystrA**: The aggregate of the most recent votes for candidate A.
- **lexpendA**: Logarithm of expandA.
- **lexpendB**: Logarithm of expandB.
- **shareA**: The percentage of campaign expenditure by candidate A out of the sum of expenditures by candidates A and B.

## Methodology
1. **Data Preprocessing**:
   - Encoded categorical variables (e.g., State) using one-hot encoding.
   - Removed duplicate rows and handled missing values.
   - Detected and removed outliers using the Interquartile Range (IQR) method.

2. **Exploratory Data Analysis (EDA)**:
   - Visualized the distribution of variables using histograms.
   - Analyzed relationships between variables using scatter plots and correlation heatmaps.

3. **Regression Analysis**:
   - Performed Ordinary Least Squares (OLS) regression to model the relationship between campaign expenditures and voting outcomes.
   - Evaluated the significance of independent variables using t-tests and p-values.

## Key Findings
- **Positive Correlation**: There is a positive correlation between campaign expenditures by candidate A (`expandA`, `lexpendA`) and the percentage of votes received (`voteA`).
- **Negative Correlation**: Higher campaign expenditures by candidate B (`expandB`) are associated with fewer votes for candidate A.
- **Significant Variables**: Variables such as `prtystrA` (party strength) and `democA` (party affiliation) are significant predictors of voting outcomes.
- **Diminishing Returns**: The relationship between campaign spending and voting outcomes shows diminishing returns, indicating that increased spending has a smaller impact as spending grows.

## Regression Models
1. **Model 1**:
   - **R-squared**: 0.943
   - **Significant Variables**: `expandA`, `prtystrA`, `shareA`, and state indicators.
   - **Interpretation**: 94.3% of the variance in voting outcomes is explained by the model.

2. **Model 2**:
   - **R-squared**: 0.951
   - **Significant Variables**: `lexpendA`, `prtystrA`, `democA`.
   - **Interpretation**: A 1% increase in campaign expenditure by candidate A leads to a 6.24% increase in votes, holding other variables constant.

3. **Model 3**:
   - **R-squared**: 0.946
   - **Significant Variables**: `lexpendA`, `expandA`.
   - **Interpretation**: The relationship between campaign spending and voting outcomes is positive but shows diminishing returns.

## Conclusion
The analysis reveals that campaign expenditures significantly impact voting outcomes, with diminishing returns as spending increases. Party strength and affiliation also play crucial roles in determining election results. These findings can help political candidates and strategists optimize campaign spending and resource allocation.

## Repository Structure
- **Project-Report.pdf**: Detailed report of the analysis.
- **Voting_Outcomes_and_Campaign_Expenditures.csv**: Dataset used for the analysis.
- **README.md**: Overview of the project (this file).

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. Open the Jupyter Notebook or Python script to explore the analysis.
3. Refer to `Project-Report.pdf` for detailed insights and findings.

## Dependencies
- Python 3.x
- Libraries: `pandas`, `numpy`, `scipy`, `statsmodels`, `matplotlib`, `seaborn`

## Author
- **Farid Mohammadzadeh**
- **Supervisor**: Dr. Mahsa Jahandideh



For any questions or further information, please contact [Farid Mohammadzadeh](mailto:frdmohammadzadeh@gmail.com).
