# Modern Portfolio Theory – Portfolio Construction & CAPM Analysis  

This project applies **Modern Portfolio Theory (MPT)** and **CAPM** to construct and evaluate optimal portfolios using a mix of domestic and international equities. This project demonstrates the practical application of portfolio optimization theory, highlighting how diversification, correlation structure, and leverage constraints influence portfolio construction and risk-adjusted performance.


---

## Project Objective  

The goal of this project is to:

- Construct **Minimum Variance** and **Tangency (Maximum Sharpe Ratio)** portfolios  
- Compare domestic-only portfolios with portfolios including an international asset (Apple)  
- Analyze diversification benefits through correlation and covariance structures  
- Evaluate individual securities using **CAPM-based required returns**  
- Study the impact of realistic short-selling constraints  

---

## Securities Considered  

### Domestic Stocks
- Sun Pharma  
- SBI  
- Eternal  
- Infosys  
- Hindustan Unilever  

### International Stock
- Apple  

Historical price data was sourced using `yfinance`.

---

## Methodology  

### 1. Modern Portfolio Theory (MPT)

- Computed expected annualized returns  
- Calculated annualized volatility  
- Constructed covariance and correlation matrices  
- Generated the efficient frontier  
- Identified:
  - **Minimum Variance Portfolio**
  - **Tangency Portfolio (Maximum Sharpe Ratio)**  

Two portfolio configurations were analyzed:

1. Domestic-only portfolio  
2. Domestic + Apple (International diversification)  

**Observation:**  
Adding Apple significantly improved the risk-adjusted return, shifted the efficient frontier outward, and increased the slope of the Capital Allocation Line.

---

### 2. Short-Selling Constraints  

The following constraints were imposed:

1. Maximum short position in a single stock ≤ 100% of portfolio value  
2. Sum of absolute portfolio weights ≤ 200% (leverage cap)  

These constraints were designed to reflect realistic market exposure limits inspired by:
- SEBI position limits  
- Basel III leverage principles  

---

### 3. CAPM Analysis  

For each domestic stock:

- Calculated required return using CAPM  
- Compared required return with historical annualized return  
- Classified stocks as:
  - **Undervalued (Buy)**  
  - **Overvalued (Sell)**  

**Findings:**
- Sun Pharma, SBI, Eternal, and Infosys appeared undervalued  
- Hindustan Unilever appeared overvalued  

---

## Key Results  

- International diversification materially improved expected return and Sharpe ratio.  
- The international tangency portfolio delivered significantly better risk-adjusted performance than the domestic-only portfolio.  
- Maximum observed covariance (~0.23) was relatively low, consistent with MPT assumptions.  
- Short-selling constraints did not materially distort minimum variance allocations due to limited exploitable covariance.  


---

## Tools & Libraries  

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- SciPy  
- yfinance  

---

## References  

- Yahoo Finance  
- SEBI Guidelines  
- Basel III Norms  
- Course material on Modern Portfolio Theory & CAPM  
