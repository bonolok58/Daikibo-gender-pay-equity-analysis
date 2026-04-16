# Daikibo-gender-pay-equity-analysis
Excel-based analysis of gender pay equality using classification logic
# Daikibo Gender Pay Equality Analysis (Excel)

## 📊 Overview
This project analyzes gender pay equality across different factories and job roles at Daikibo Industrials.

Using a provided dataset, the goal was to classify job roles based on how balanced compensation is between genders.

---

## 🎯 Objectives
- Analyze equality scores across factories and job roles
- Classify each role into fairness categories
- Highlight areas of potential pay discrimination

---

## 🛠 Tools Used
- Microsoft Excel

---

## 📁 Dataset
The dataset contains:
- Factory
- Job Role
- Equality Score (range: -100 to +100)

Where:
- 0 represents perfect equality
- Negative values indicate potential bias in one direction
- Positive values indicate bias in the opposite direction

---

## ⚙️ Methodology

A new column called **"Equality Class"** was created using a formula based on the absolute value of the Equality Score:

```excel
=IF(ABS(C2)<=10,"Fair",
   IF(ABS(C2)<=20,"Unfair",
   "Highly Discriminative"))
