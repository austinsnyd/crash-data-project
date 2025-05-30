# 🚦 Crash Data Analysis in New Zealand (2009)

This project analyzes crash patterns involving **motorcyclists**, **pedestrians**, and **bicyclists** in New Zealand using 2009 data from the VGAM R package. The analysis aims to inform road safety efforts and assess the relative risk of different transportation modes based on time of day and day of week.

---

## 📊 Project Objectives

1. **How dangerous is riding a motorcycle as a primary means of transportation?**
2. **Are motorcycles the most common means of transportation involved in crashes on weekends?**

---

## 📁 Data Source

The analysis uses crash data matrices provided by the `VGAM` package:

- `crashmc` – Motorcycle crashes  
- `crashp` – Pedestrian crashes  
- `crashbc` – Bicycle crashes

Each matrix is structured by **hour (0–23)** and **day (Mon–Sun)**.

---

## 🛠️ Methods

### 📌 Data Wrangling

- Combined and transformed all matrices into a single long-format dataset
- Key variables: `Type`, `Day`, `Hour`, `Count`

### 🔍 Statistical Modeling

- **Poisson Regression** to model crash counts
- **Negative Binomial Regression** to address overdispersion
- Modeled interactions: `Type × DayGroup × TimeCategory`

### 🧪 Model Evaluation

- Compared models using:
  - AIC / BIC
  - Residual diagnostics
  - Mean Squared Prediction Error (via k-fold CV)

---

## 📈 Key Insights

- **Motorcyclists** face the highest predicted crash counts, especially:
  - During weekday **morning and evening commutes**
  - During **weekend afternoons**
- Motorcycles are the **most common** vehicle type involved in weekend crashes (aside from cars)

---

## 🔮 Future Work

- Incorporate variables like weather, road conditions, and traffic volume
- Propose policy recommendations targeting high-risk times
- Explore time-series modeling for crash forecasting

---

## 🧾 Technologies Used

- **R**: `tidyverse`, `VGAM`, `MASS`, `flexplot`, `ggplot2`
- **R Markdown** for reproducible reporting

