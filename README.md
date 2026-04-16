Strategic Framework for Predictive Maintenance (PdM):
Engineering Reliability & Financial Lifecycle Valuation of Industrial Assets

By Cajethan Nwangwu | April 16, 2026 

Project Overview:

Unplanned downtime in the oil and gas sector can cost between $200,000 and $500,000 per hour. This project implements a robust predictive maintenance framework using the NASA Turbofan Engine Degradation Simulation Dataset (C-MAPSS) to move beyond "Run-to-Failure" strategies.
By merging chemical engineering principles (thermodynamic efficiencies) with data analytics, this model identifies early degradation signals on the PF curve to prevent functional failure and secondary system damage.

Technical Stack:

•	Language: R

•	Core Libraries: 

i) tidyverse: Data wrangling and visualization 
ii) tidymodels: Reproducible machine learning framework 
iii) slider: Feature engineering for rolling window statistics 
Iv) PerformanceAnalytics: Multi-variate sensor correlation analysis 

The "Engineering Edge": Feature Engineering

The core predictive power of this model is derived from transforming raw sensor readings into temporal features that capture the velocity of degradation.
•	Remaining Useful Life (RUL): Calculated as the difference between the maximum cycle and the current cycle for each unit.
•	Rolling Statistics: Used a 5-cycle rolling average for critical sensors (e.g., s_11/Ps30 and s_15/Bypass Ratio) to act as a low-pass filter, smoothing operational noise.
•	Classification: The model predicts a "High Risk" status for any unit expected to fail within the next 30 days/cycles.

Model Performance & Validation:
We utilized a Random Forest model via the ranger engine, chosen for its ability to capture non-linear interactions between thermodynamic parameters.
 
ROC Curve Analysis:

The model demonstrates high discriminative power, as evidenced by the Receiver Operating Characteristic (ROC) curve.
•	High Sensitivity: The model successfully identifies the majority of imminent failures ("High Risk" units) before they occur.
•	Low False Positive Rate: Minimizes "unnecessary maintenance" on healthy machines, preserving OPR (Overall Plant Reliability).
•	AUC: The curve achieves high proximity to the top-left corner, indicating a high AUC (likely >0.95) and reliable decision-making capability.

Economic & Strategic Impact:

Adopting this PdM framework addresses the "40x cost difference" between emergency and planned repairs:
•	Planned Repair: Approx. $6,500.
•	Emergency Repair: Upwards of $261,000 (factoring in production losses).

Repository Structure:

•	/data: Information on accessing the C-MAPSS dataset.
•	/scripts: R scripts for data extraction, feature engineering, and model training.
•	/report: Detailed PDF report on the strategic and thermodynamic context.
________________________________________Contact: [http://www.linkedin.com/in/cajethan-nwangwu /nwangwucajethan85@gmail.com]
