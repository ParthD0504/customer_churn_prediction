# Customer Churn Risk Segmentation

A Jupyter-based data analysis and clustering pipeline to identify at-risk customers by leveraging transaction data and RFM (Recency–Frequency–Monetary) modeling. By segmenting customers into behavioral cohorts, we can flag those most likely to churn and target retention efforts accordingly.

---

## 📋 Project Structure

```
├── customer_churn.ipynb      # Main notebook: EDA → RFM feature engineering → clustering
├── project2_data.csv         # Raw transaction data
└── README.md                 # Project overview and instructions
```

---

## 🎯 Objectives

1. **Explore & Clean**  
   – Load transaction dataset  
   – Handle cancellations and invalid entries  
   – Derive useful time-based features (Year, Month, Day, Recency)  

2. **Feature Engineering (RFM)**  
   – **Recency**: Days since last purchase  
   – **Frequency**: Total number of purchases  
   – **Monetary**: Total spend per customer  

3. **RFM Scoring & Customer Segmentation**  
   – Assign 1–4 scores per RFM metric using quartiles  
   – Combine into composite RFM score  
   – Use Elbow method & K-Means to cluster customers into 6 behavioral groups  

4. **Insights & Visualization**  
   – Cluster profiling (e.g., “Loyal”, “At-Risk”, “Churned”)  
   – Product, time-series, geographic, payment method, and refund analyses  
   – Visual dashboards with Matplotlib & Seaborn  

---

## 🛠️ Installation

1. Clone this repository  
   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```

2. (Optional) Create a virtual environment  
   ```bash
   python3 -m venv venv
   source venv/bin/activate    # Linux/Mac
   venv\Scripts\activate       # Windows
   ```

3. Install dependencies  
   ```bash
   pip install -r requirements.txt
   ```

---

## 🚀 Usage

1. **Download or place** `project2_data.csv` in the project root.  
2. **Launch** Jupyter Lab/Notebook:
   ```bash
   jupyter lab
   ```
3. **Open** `customer_churn.ipynb` and execute all cells in order.  
4. **Inspect** the final cluster outputs and visualizations to identify at-risk segments.

---

## 📈 Key Findings

- **Cluster Profiles**:  
  - **Cluster 0**: High recency, low frequency → **Potential churners**  
  - **Cluster 1**: Low recency, high monetary → **Loyal, high-value customers**  
  - … _(other clusters detailed in notebook)_  

- **Top-Returning Products**: Identified top 10 SKUs with highest cancellation rates.  
- **Seasonal Trends**: Peak purchasing months and days highlighted.  
- **Geographic Hotspots**: Countries with most active vs. churn-prone customer bases.  

Use these insights to tailor retention campaigns, loyalty rewards, and re-engagement offers.

---

## 📦 Dependencies

- Python 3.8+  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- yellowbrick  


---

## ✉️ Author

**Parth Deshmukh**  
– MS in Data Analytics Engineering, Northeastern University (’25)  
– GitHub: [github.com/ParthD0504](https://github.com/ParthD0504)  
– Contact: deshmukh.par@northeastern.edu  
