# 📊 Mean Reversion & Stationarity Analysis: Sensex vs Nifty

This project investigates the **mean-reverting behavior** between India's major stock indices – **Sensex** and **Nifty**. By constructing a statistical spread and applying formal time-series tests, we assess whether this spread is stationary, which indicates a potential long-run equilibrium relationship.

---

## 🔍 Objective

To determine if the spread defined by:

Spread = Sensex − x × Nifty

is **stationary** — a key condition for long-term market equilibrium and pair-based trading strategies.

---

## 🧪 Methodology

### 📉 1. OLS Regression (Hedge Ratio Estimation)
We run an **Ordinary Least Squares (OLS)** regression of Sensex on Nifty:
```python
Sensex = α + x × Nifty + ε
Here, x is the hedge ratio — it defines the linear relationship between Sensex and Nifty. The residuals from this regression (i.e., the spread) are further analyzed for stationarity.


2. Spread Calculation
Once x is estimated, the spread is calculated as:

Spread = Sensex - x × Nifty
This spread is the focus of our stationarity testing.

3. Augmented Dickey-Fuller (ADF) Test
The ADF test is used to check if the spread is stationary.

Null Hypothesis (H₀): The series has a unit root (non-stationary)

Alternative Hypothesis (H₁): The series is stationary

A p-value < 0.05 allows us to reject H₀ and conclude that the spread is stationary.

To standardize the spread, we compute its Z-score:

python
Copy
Edit
Z = (Spread − mean) / std
This helps identify how far the spread deviates from its mean, useful for visual inspection of mean reversion.

![image](https://github.com/user-attachments/assets/a23fc24e-6dfa-4c8d-bd45-85ff01e3f1ef)

![image](https://github.com/user-attachments/assets/09919c3d-b665-45a1-8d60-268d93de9f33)

