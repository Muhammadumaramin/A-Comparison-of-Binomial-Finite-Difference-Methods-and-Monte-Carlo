# 📘 American Option Pricing: Binomial Tree, Monte Carlo (LSM), and Finite Difference (Crank–Nicolson)

### **Authors:**  
**Muhammad Umar Amin**  
**A K M Intisar Islam**  
Department of Mathematics, Lamar University  
Course: **MATH 5315 – Numerical Analysis**  
Date: **November 2025**

---

## 📖 Overview

American-style options introduce a major computational challenge due to their **early exercise feature**, which turns pricing into a **free-boundary / optimal-stopping problem**.

This project develops and compares three major numerical techniques used in quantitative finance:

1. **Binomial Tree (CRR/Tian)**
2. **Monte Carlo Simulation (Longstaff–Schwartz LSM)**
3. **Finite Difference Method (Crank–Nicolson PDE solver)**

A synthetic dataset of **500 American call and put options** was generated to evaluate each model’s accuracy, convergence, and computational performance.

---

## 🧠 Methods Implemented

### **1. Binomial Tree Method**
- Implements Cox–Ross–Rubinstein with Tian’s variance adjustment.  
- Handles early exercise naturally through backward induction.  
- Achieved the most accurate results in this study.

### **2. Monte Carlo Simulation (Longstaff–Schwartz LSM)**
- Simulates thousands of price paths via geometric Brownian motion.  
- Uses polynomial regression to approximate continuation values.  
- Effective for high-dimensional or path-dependent derivatives.

### **3. Finite Difference Method (Crank–Nicolson)**
- Solves the Black–Scholes PDE on a discretized grid.  
- Incorporates early exercise using a linear complementarity constraint.  
- Accuracy sensitive to grid resolution and boundary conditions.

---

## 📊 Dataset

- 500 synthetic American options (calls & puts)
- Features:
  - Underlying price \(S_0\)
  - Strike price \(K\)
  - Volatility \(\sigma\)
  - Dividend yield \(q\)
  - Risk-free rate \(r\)
  - Time-to-expiry \(T = \text{DTE} / 365\)

A high-resolution **Binomial Tree (N = 500)** served as the benchmark.

---

## 🧪 Performance Metrics

Evaluated on a 20% test split using:

- **RMSE – Root Mean Squared Error**
- **MAE – Mean Absolute Error**
- **R² – Coefficient of Determination**

### **Results Summary**

| Method | RMSE | MAE | R² |
|--------|------|------|-----|
| **Binomial Tree (N=200)** | **0.1983** | **0.1081** | **0.9996** |
| **Monte Carlo (LSM)** | 3.6599 | 1.8797 | 0.8739 |
| **Finite Difference (Crank–Nicolson)** | 7.8919 | 4.8627 | 0.4135 |

---

## 🧩 Key Insights

- ✔ **Binomial Tree** delivered the most accurate and stable option prices.  
- ✔ **Monte Carlo LSM** performed well with moderate variance due to stochastic sampling.  
- ✔ **Finite Difference CN** underpriced options on coarse grids, highlighting discretization sensitivity.  
- ✔ Each method reflects a different numerical philosophy:  
  - **Lattice (Binomial)**  
  - **Simulation + Regression (MC-LSM)**  
  - **PDE Discretization (FDM)**  

---

## 🛠️ Technologies Used

- Python  
- NumPy  
- SciPy  
- Pandas  
- Matplotlib  
- Random number simulation  
- Numerical linear algebra  
- PDE discretization  
- Regression modeling  

---

## 📂 Repository Structure

American-Option-Pricing/
│
├── binomial_tree.py
├── monte_carlo_lsm.py
├── finite_difference_cn.py
├── generate_dataset.py
├── compare_models.py
│
├── figures/
│ ├── binomial_scatter.png
│ ├── mc_scatter.png
│ ├── fd_scatter.png
│ └── ...
│
└── README.md

---

## 📚 References

- Cox, Ross & Rubinstein (1979) – Binomial option pricing model  
- Longstaff & Schwartz (2001) – Least-Squares Monte Carlo  
- Wu & Kwok (1997) – Front-fixing PDE approach  
- Zhao, Davison & Corless (2007) – Improved finite difference schemes  
- Kim, Kim & Song (2024) – Modern American option algorithms  
- Thomas (2013); Duffy (2013) – Numerical PDE literature  

---

## 🏁 Conclusion

This project demonstrates how three foundational numerical methods behave when applied to American option pricing:

- **Binomial Tree** → most accurate and robust  
- **Monte Carlo LSM** → most flexible for higher dimensions  
- **Finite Difference CN** → most sensitive but mathematically elegant  

It reflects strong skills in **quantitative finance, numerical computation, stochastic modeling, and PDE-based methods**.

---

## 📬 Contact

For questions, collaboration, or improvements, feel free to reach out.
https://www.linkedin.com/in/mumaramin-0a6795257/

