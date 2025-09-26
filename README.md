# Porfolio Optimization Using Data Science (Python and SciPy)
The project demonstrates Pertfolio Optimization.
The goal is to find the ideal allocation of assets that maximizes the risk-adjusted return, as measured by the Sharpe Ratio. The project uses a direct mathematical optimization approach with the SciPy library.

The core of this project is to solve a constrained optimization problem: finding the portfolio weights (wi
​
 ) that maximize the Sharpe Ratio.
```math
\begin{align*}
& \text{} \quad \text{Sharpe Ratio} = \frac{R_p - R_f}{\sigma_p}
\end{align*}
```


## Project Workflow

This project follows a concise and linear workflow, all contained within the `Portfolio_Optimization.ipynb` notebook:

1.  **Data Acquisition**: Fetches 5 years of historical price data for a selected basket of stocks (`AAPL`, `GOOGL`, `MSFT`, `JPM`, `V`) directly from Yahoo Finance.
2.  **Metric Calculation**: Processes the raw price data to calculate the two critical inputs for our model:
    * **Expected Annual Returns**
    * **Annual Covariance Matrix**
3.  **Mathematical Optimization**:
    * Defines an objective function to calculate the portfolio's Sharpe Ratio.
    * Uses the `scipy.optimize.minimize` function to find the exact weights that maximize this objective, subject to our constraints.
4.  **Results & Visualization**:
    * Presents the final, optimal asset allocation in a clear, readable format.
    * Visualizes the results with a pie chart for asset allocation.

