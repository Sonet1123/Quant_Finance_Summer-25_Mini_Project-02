# Mini Project 2: Hypothesis Testing of Standard Assumptions Theoretical Financial Mathematics


## Project Overview

In this mini project, we investigate whether the commonly assumed normal distribution of log returns holds for real financial data. We analyze daily stock log returns, test for normality under various conditions, and construct portfolios with improved normal behavior.

We use Python for data collection, statistical testing, and visualization, applying several well-known tests for normality on stock log returns.

---

## Dataset

- **Period:** Past 5 years of daily data
- **Stocks Analyzed:**
  - AAPL, MSFT, GOOGL, TSLA, NVDA, KO, JNJ, PG, PEP, XOM
- **Source:** Fetched using `yfinance`
- **Returns Computed:** Daily log returns  
  \[
  r_t = \log\left( \frac{P_t}{P_{t-1}} \right)
  \]

---

##  Tasks Completed

### **Task 1:** Rolling Window Normality
- Applied Anderson–Darling test on 126-day rolling windows.
- Stocks like XOM and AAPL showed local normality.
- XOM passed in 80% of the rolling windows.

### **Task 2:** Normality After Removing Extremes
- Removed top/bottom 3% of return values.
- Re-tested normality using Shapiro-Wilk, Jarque-Bera, and Anderson–Darling tests.
- Stocks like XOM, KO, and TSLA showed significantly improved results.

### **Task 3:** Building a Normally Distributed Portfolio
- Selected 5 stocks with best test performance after trimming.
- Constructed equal-weight portfolio.
- Portfolio passed all three normality tests.

### **Task 4:** Analyzing Portfolios from Mini Project 1
- Tested high-risk and low-risk portfolios using rolling window normality.
- High-Risk: ~80.85% windows passed
- Low-Risk: ~69.86% windows passed

### **Task 5:** Full-Period Normality on Individual Stocks
- All 10 stocks tested for normality over full 5-year period.
- None passed all tests; visual plots confirmed heavy tails and non-Gaussian behavior.

---

## Statistical Methods Used

- **Shapiro–Wilk Test**
- **Jarque–Bera Test**
- **Anderson–Darling Test**
- **Rolling Window Analysis**
- **Data Trimming (3%)**
- **Portfolio Return Construction**

---

## Repository Contents

| File                      | Description                                        |
|---------------------------|----------------------------------------------------|
| `Mini Project 2.ipynb`          | Full analysis notebook with code and results      |
| `Report_Mini_Project-2.pdf`     | Final report in PDF format (LaTeX-generated)       |


---

##  Tools & Libraries

- Python, Jupyter Notebook
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scipy.stats`, `statsmodels`
- `yfinance` for stock data

---

##  Key Takeaways

- Log returns are rarely normally distributed over long periods.
- Many stocks exhibit local normality in shorter rolling windows.
- Removing outliers can significantly improve normality.
- Carefully constructed portfolios can behave more like normal distributions.

---


