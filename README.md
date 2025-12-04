# Shipwrecks Analysis — Data Science Nanodegree Project

This project is part of the Udacity **Data Scientist Nanodegree** and focuses on performing 
exploratory data analysis, data cleaning, and predictive modeling on an open-source dataset 
of Roman-era shipwrecks from ProjectMercury.eu. The goal of the project is to understand 
patterns within the shipwreck data and build a machine learning model capable of predicting 
a shipwreck’s estimated depth based on available features.

---

## Libraries Used

This project uses the following Python libraries:

- **pandas** — data loading, manipulation, cleaning  
- **numpy** — numerical operations  
- **matplotlib** — visualization  
- **seaborn** — statistical visualizations  
- **scikit-learn** — model training, evaluation, and prediction  

All dependencies are listed in the `requirements.txt` file.

---

## Project Motivation

Shipwrecks provide valuable archaeological insights into trade, warfare, transportation, and 
economic activity across the ancient Mediterranean. Understanding depth, location, and 
ship characteristics can assist marine archaeologists in:

- Estimating how environmental and physical features relate to shipwreck locations  
- Predicting how deep newly discovered wrecks might be  
- Exploring correlations between age, tonnage, and site conditions  

The main question explored in this project is:

> **Can we predict the depth of a shipwreck using features such as latitude, longitude, estimated tonnage, and dating information?**

---

## Repository Structure

### **File Descriptions**

| File | Description |
|------|-------------|
| `analysis.ipynb` | Contains the full analysis pipeline: EDA, cleaning, model training, evaluation, and the fictional prediction scenario required by Udacity. |
| `shipwrecks.csv` | Dataset used for the project, including coordinates, estimated tonnage, dating ranges, and depth information where available. |

---

## Summary of Results

### **Exploratory Findings**
- Several variables showed skewed distributions, particularly depth and estimated tonnage.  
- Moderate correlations were observed between depth and geographic coordinates.  
- Some variables (e.g., Min depth vs Max depth) displayed clear linear relationships.  
- Missing values were present but manageable using median imputation.

### **Model Performance**
A linear regression model was trained to predict shipwreck depth:

- **R² Score:** *approximate value here*  
- **RMSE:** *approximate value here*  
- **MAE:** *approximate value here*

The linear regression model demonstrated limited accuracy and occasionally produced 
non-physical predictions (e.g., negative depths). This highlighted the limitations of 
linear models for archaeological prediction tasks and suggests that nonlinear models 
(Random Forest, Gradient Boosting) could be explored in future work.

### **Scenario Prediction**
A fictional archaeological scenario was created, and the model was used to estimate 
the depth of a newly “discovered” shipwreck.  
After correcting for negative values (since depth must be ≥ 0), the model provided a 
plausible depth estimate based on ship tonnage, location, and dating information.

---

## Acknowledgments

- The dataset was sourced from **ProjectMercury.eu**, a public digital archaeology initiative that provides 
open and structured data on the ancient Mediterranean world.  
