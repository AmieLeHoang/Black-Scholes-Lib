# Black-Scholes Option Pricing & Sensitivity Analysis

## **Overview** 

This repository provides a robust, vectorized implementation of the Black-Scholes-Merton (BSM) model for pricing European-style options. It is designed for quantitative researchers and analysts who require precise theoretical valuations and sensitivity metrics (Greeks) for risk management and strategy backtesting.


## **Key Features**

1. European Option Pricing: Accurate valuation for both Call and Put options using the closed-form BSM solution.
2. Vectorized Greeks: High-speed computation of the first and second-order sensitivities:
     * Delta ($\Delta$): Rate of change in price relative to the underlying.
     * Gamma ($\Gamma$): Rate of change in Delta.
     * Vega ($\nu$): Sensitivity to volatility.
     * Theta ($\Theta$): Time decay.
     * Rho ($\rho$): Sensitivity to the risk-free rate.
3. Implied Volatility (IV): Solver using the Newton-Raphson method to back out market-implied volatility.
4. Visualizations: Interactive plotting of the "Volatility Smile" and Greek surfaces across varying Spot Prices and Time-to-Maturity.


## **Mathematics**

The model assumes the underlying asset follows a Geometric Brownian Motion (GBM). The price of a Call option $C$ is defined as 

$$C = S_0 N(d_1) - K e^{-rT} N(d_2)$$

Where: 

  $$d_1 = \frac{\ln(S_0/K) + (r + \sigma^2/2)T}{\sigma\sqrt{T}}$$
  
  $$d_2 = d_1 - \sigma\sqrt{T}$$

  
## **Tech Stack**

* Python 3.10 + NumPy: For vectorized numerical operations.
* SciPy: For the Cumulative Distribution Function (CDF) and optimization.
* Matplotlib/Seaborn: For sensitivity visualizations.
* Black: For PEP 8 code formatting compliance.



# Clone the repo
git clone https://github.com/AmieLeHoang/black-scholes-python.git

# Install dependencies
pip install -r requirements.txt
