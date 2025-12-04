# Maritime Fleet Optimization under Regulatory Uncertainty

**Author:** Akash Deep Jana  
**Domain:** Maritime Technology / Operations Research  
**Focus:** Digital Twins, Stochastic Modeling, EU ETS Carbon Pricing

##  Project Overview
This research develops a data-driven **Digital Twin** framework to quantify the financial risk of **EU Emissions Trading System (ETS)** compliance on fleet operations. Unlike standard fuel monitoring models, this project integrates **stochastic financial modeling** (Geometric Brownian Motion) with **physics-informed machine learning** to predict voyage costs under regulatory volatility.

##  Key Features
* **Stochastic Carbon Pricing:** Simulates EU Allowance (EUA) price trajectories ($dS_t = \mu S_t dt + \sigma S_t dW_t$) to capture market volatility ($\sigma \approx 40\%$).
* **Physics-Informed ML:** Implements **XGBoost** with monotonic constraints to capture non-linear hydrodynamic effects (e.g., drag humps in planing hulls, SFOC penalties).
* **Digital Twin Logic:** Enriches raw operational data with synthetic "real-world" variables like hull fouling (days since drydock) and sea state impact.

##  Methodology
1.  **Data Enrichment:** Synthetic generation of missing physics variables (Speed vs. Power curves) based on vessel type (Tanker vs. Surfer Boat).
2.  **Modeling:** Comparison of **Linear Regression (Baseline)** vs. **XGBoost (Champion)**.
3.  **Validation:** Physics-based sanity check using the **Admiralty Coefficient** ($A_c = \Delta^{2/3}V^3/P$) to ensure the model adheres to naval architectural principles.

##  Results
* **Accuracy:** The XGBoost model significantly outperformed the linear baseline by capturing the "bathtub curve" of Specific Fuel Oil Consumption (SFOC) at low engine loads.
* **Physics Check:** Validated that predicted fuel consumption scales correctly with speed ($R \propto V^3$ for displacement hulls), confirming the model's reliability for operational decision-making.

##  Repository Contents
* `Maritime_Fleet_Optimization.ipynb`: Complete Python workflow (Data Generation -> Modeling -> Evaluation).
* `Project_Report.pdf`: Full academic report summarizing the research context and findings.

---
*This project serves as a technical portfolio piece for doctoral research in Maritime Fleet Optimization.*
