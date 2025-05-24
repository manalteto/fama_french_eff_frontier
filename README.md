# Fama-French Four-Factor Efficient Frontier

This project enhances a mean-variance portfolio optimization by recalculating expected returns using the **Fama-French four-factor model**. It replaces the unrealistic historical mean return assumption with factor-based expected returns, providing a more robust framework for evaluating the Telfer Capital Fund's stock holdings.

## Objectives

- Download and merge Fama-French factor data with historical stock returns
- Estimate factor betas for each stock using OLS regression
- Compute expected returns with the Equation below
- Rebuild the efficient frontier using these expected returns
- Compare new vs. original frontier based on mean returns
  
  $$
E[R_i] = R_f + \beta_{\text{mkt}}(R_m - R_f) + \beta_{\text{SMB}} \cdot \text{SMB} + \beta_{\text{HML}} \cdot \text{HML} + \beta_{\text{MOM}} \cdot \text{MOM}
$$

Where:  
- $E[R_i]$: Expected return of stock $i$  
- $R_f$: Risk-free rate  
- $R_m$: Market return  
- $(R_m - R_f)$: Market risk premium  
- $\beta_{\text{mkt}}$: Sensitivity to the market factor  
- $\beta_{\text{SMB}}$: Sensitivity to the size factor (Small Minus Big)  
- $\beta_{\text{HML}}$: Sensitivity to the value factor (High Minus Low)  
- $\beta_{\text{MOM}}$: Sensitivity to the momentum factor (past winners minus losers)  
- $SMB$, $HML$, $MOM$: Fama-French factor premiums

## Tools & Data

- Python (`pandas`, `numpy`, `statsmodels`, `matplotlib`)
- WRDS/CRSP for stock returns
- Kenneth French Data Library for factor data

## Key Results

- Factor-based expected returns are typically lower and more conservative than historical means
- Efficient frontier is shifted and reshaped, reflecting updated return assumptions
- Tangency portfolio and optimal weights are recalculated under the new model

## Interpretation

This approach grounds expected return estimates in economic theory, improving realism and robustness. It also highlights how return estimation techniques can significantly affect portfolio construction outcomes.


