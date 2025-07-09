# Redbus Data Hackathon 2025 – Demand Forecasting Project

## Overview

This repository contains our solution for the **Redbus Data Hackathon 2025**, focused on forecasting the **number of travellers for a specific journey date**, 15 days in advance. Our team ranked **52 out of 694 participants**, showcasing our approach's effectiveness in tackling this real-world forecasting challenge in the transportation industry.

## Problem Statement

In the bus transportation industry, less than 20% of bookings are made well in advance. This makes demand forecasting particularly challenging due to sparse early signals. Accurate forecasts play a vital role in shaping:

- Pricing strategies
- Marketing and SEO efforts
- Discounting schemes

The hackathon challenged participants to **develop machine learning models that accurately forecast the final seat count** for various routes and journey dates, using a combination of route metadata and transaction history.

---

## Our Approach

We developed a modular and extensible pipeline built around the `BusBookingPredictor` class, handling all stages from data loading to ensemble prediction.

### Key Steps:

1. **Data Loading & Preparation**
   - Inputs: `train.csv`, `test.csv`, `transactions.csv`
   - Preprocessing and basic filtering

2. **Feature Engineering**
   - Date-based features
   - Aggregated booking statistics
   - Route-level transformations

3. **Categorical Encoding**
   - Label encoding of route identifiers, source/destination IDs, etc.

4. **Model Training**
   - Trained multiple models using:
     - LightGBM
     - XGBoost
     - CatBoost
   - Used validation split for robust evaluation

5. **Ensemble Modeling**
   - Combined predictions using a weighted ensemble to enhance accuracy

6. **Feature Importance**
   - Extracted and visualized top 20 most impactful features

---

## 📁 Project Structure

```bash
.
├── train.csv
├── test_8gqdJqH.csv
├── transactions.csv
├── submission_file_NN.csv
├── bus_booking_predictor.py     # Contains the BusBookingPredictor class
├── main.py                      # The main script (code provided above)
├── README.md                    # This file
How to Run
Clone this repository:

bash
Copy
Edit
git clone https://github.com/yourusername/redbus-demand-forecasting.git
cd redbus-demand-forecasting
Install required dependencies:

bash
Copy
Edit
pip install pandas numpy scikit-learn lightgbm xgboost catboost
Place the datasets (train.csv, test_8gqdJqH.csv, transactions.csv) in the root directory.

Run the main script:

bash
Copy
Edit
python main.py
Output:

The final predictions will be saved in: submission_file_NN.csv

📌 Results
Leaderboard Rank: 52 / 694

Evaluation Metric: [RMSE]

Public Score: [617]


Learnings
Handling sparse time series data with low early signal.

Balancing overfitting vs underfitting in time-sensitive data.

Applying ensemble learning to improve prediction robustness.

Credits
Developed by: [Strive in Dark Team / Durga Ram Prasad Bhandari, Irum Hussain , Sai Kumar Bashetti ]

Contact: 

Rank Achieved: Top 8% globally (52/694)

Contact & Opportunities
If you're interested in collaborating, feel free to connect or drop a message!

LinkedIn: [https://www.linkedin.com/in/irum-hussain-4b3957140/]

