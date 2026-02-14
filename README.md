# 📊 Food Delivery Delay Analysis

## 🔍 Overview

This project analyses food delivery order data to identify the **primary drivers of delivery delays**.  
The objective is to determine whether delays are primarily caused by restaurant operations or by external factors such as weather and peak-hour demand.

The analysis focuses on **root-cause identification and operational impact**, rather than predictive modelling.

---

## 🎯 Business Problem

Delayed food deliveries negatively impact:

- Customer satisfaction  
- Platform reputation  
- Operational efficiency  
- Revenue growth  

The goal of this analysis is to:

- Quantify the extent of delivery delays  
- Identify the dominant contributors  
- Evaluate the effect of weather and peak-hour demand  
- Provide actionable business recommendations  

---

## 📂 Dataset

- **Type:** Synthetic dataset (created for learning and portfolio purposes)  
- **Records:** 500 food delivery orders  
- **Purpose:** Simulate realistic operational scenarios  

### Key Variables

| Column | Description |
|--------|------------|
| `order_id` | Unique identifier for each order |
| `restaurant_prep_time` | Time taken by restaurant to prepare order (minutes) |
| `delivery_time` | Time taken to deliver order (minutes) |
| `distance_km` | Distance between restaurant and customer |
| `weather` | Weather condition (Clear / Rain) |
| `peak_hour` | Whether order was placed during peak hours |
| `delayed` | Delivery outcome (1 = Delayed, 0 = On-time) |

> ⚠️ Note: This dataset is synthetic and used strictly for analytical demonstration purposes.

---

## 🛠 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Gemma-AI
---

## 📊 Key Findings

### 1️⃣ Overall Delay Rate
- **61% of orders were delayed**, indicating a systemic operational issue.

---

### 2️⃣ Preparation Time Is the Dominant Driver

| Order Status | Avg Prep Time |
|--------------|--------------|
| On-time | ~19.5 minutes |
| Delayed | ~33.0 minutes |

Delayed orders required **13+ additional minutes of preparation time**, identifying restaurant efficiency as the primary bottleneck.

---

### 3️⃣ The 30-Minute Threshold

| Preparation Time | Delay Rate |
|------------------|-----------|
| ≤ 30 minutes | ~28% |
| > 30 minutes | ~100% |

Orders exceeding **30 minutes of preparation time were almost always delayed**, making this a critical operational benchmark.

---

### 4️⃣ Weather Impact (Prep Time ≤ 30 Minutes)

| Weather | Delay Rate |
|---------|-----------|
| Clear | ~24% |
| Rain | ~39% |

Even during rain, over **60% of orders were delivered on time** when preparation time was controlled.

---

### 5️⃣ Peak Hour Impact (Prep Time ≤ 30 Minutes)

| Peak Hour | Delay Rate |
|-----------|-----------|
| No | ~24% |
| Yes | ~33% |

Peak-hour demand increases delay probability, but efficient preparation still ensures majority on-time delivery.

---

## 🧠 Core Insight

Restaurant preparation time is the **strongest determinant of delivery delays**.  

External factors such as weather and peak-hour demand increase risk, but their impact is significantly reduced when preparation times remain under 30 minutes.

---

## 📌 Business Recommendations

1. Enforce preparation time SLAs (≤ 30 minutes)  
2. Implement real-time preparation monitoring  
3. Allocate additional delivery resources during rain and peak hours  
4. Track and support underperforming restaurant partners  

---

## 📁 Project Structure

```
food-delivery-delay-analysis/
│
├── data/
│   └── food_delivery_data.csv
│
├── notebooks/
│   └── food_delivery_eda.ipynb
│
├── report/
│   └── Food_Delivery_Delay_Analysis_Report.pdf
│
├── requirements.txt
│
└── README.md
```

---

## 🚀 How to Run the Project

1. Clone the repository  
2. Install dependencies:

```
pip install -r requirements.txt
```

3. Open the notebook:

```
jupyter notebook
```

4. Run all cells to reproduce the analysis  

---

## 📄 Detailed Report

The full structured business report is available here:

`Report/Food-Delivery-Delay-Analysis-Report(1).pdf`

---

## 🔮 Areas for Future Analysis

- Rider availability patterns  
- Traffic congestion impact  
- Order batching optimisation  
- Seasonal demand variation  

---

## 👤 Author

**Devanshu Garad**  
