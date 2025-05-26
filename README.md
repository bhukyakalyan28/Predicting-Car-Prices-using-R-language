# 🚗 Car Price Prediction Using Machine Learning in R

This project focuses on predicting the price of used cars based on various features using two machine learning models: **Gradient Boosting Machine (GBM)** and **Decision Tree**, developed in R. It includes end-to-end steps from data cleaning and exploration to model evaluation and predictions.

---

## 📁 Dataset

**Source**: [Kaggle - Used Car Price Predictions Dataset](https://www.kaggle.com/datasets/harikrishnareddyb/used-car-price-predictions)  
**Records**: ~121,000  
**Final Sample Used**: 10,000 randomly sampled rows for efficiency

**Key Features:**
- `Price` (target)
- `Mileage`, `Year`
- `City`, `State`, `Make`, `Model`
- `Vin` (removed during preprocessing)

---

## 🔧 Technologies & Libraries

- **Language**: R
- **Packages**:
  - `dplyr`, `ggplot2`, `tidyverse`, `caret`
  - `rpart` for decision trees
  - `gbm` for gradient boosting
  - `DescTools` for winsorization
  - `forcats` for factor level grouping
  - `stringr` for string operations

---

## 📊 Data Processing & Cleaning

- Converted categorical variables to factors
- Removed unnecessary columns like VIN
- Applied **Winsorization** to cap outliers in `Mileage` and `Price`
- Lumped rare cities using `fct_lump()` (top 50 cities retained)
- Verified for missing values (none found)

---

## 📈 Exploratory Data Analysis

- **Boxplots**: Checked for outliers
- **Histograms**: Examined distribution of `Mileage` and `Price`
- **Scatter Plot**: Explored relationship between `Mileage` and `Price`
- **Bar Plot**: Visualized car count by `State`

---

## 🤖 Models Built

### 🔹 Decision Tree (rpart)
- MAE: `3566.25`
- MSE: `22,644,828.58`
- R²: `0.7991`

### 🔹 Gradient Boosting Machine (gbm)
- MAE: `2054.81`
- MSE: `8,857,565.91`
- R²: `0.9214`
- **Top Predictors**: `Model`, `Mileage`, `Year`

**Conclusion**: GBM performed better on all metrics.

---

## 📌 How to Run

### 🔹 Prerequisites

Install R and RStudio (if not already installed).

### 🔹 Steps

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/car-price-prediction.git
    cd car-price-prediction
    ```

2. **Open the R script**:
    - Use `Final_proj.R` or `Final_proj.Rmd` in RStudio.

3. **Install required packages**:
    ```r
    install.packages(c("dplyr", "ggplot2", "tidyverse", "caret", 
                       "rpart", "gbm", "DescTools", "forcats", "stringr"))
    ```

4. **Run the script**:
    - Use RStudio to run the full analysis and view visualizations.
    - Alternatively, knit the RMarkdown to PDF or HTML.

---

## 🎯 Custom Predictions

The final GBM model can be used to predict prices for new car listings. A sample dataframe with custom inputs is included in the script.

---

## 👤 Author

**Kalyan Kumar Bhukya**  
Graduate Student | Central Michigan University  
📧 bhukyakalyan28@gmail.com

---

## 📝 License

This project is for educational and non-commercial use only. Dataset belongs to its original owner on Kaggle.

---

## 📷 Screenshots (Optional)

> Add visualizations or model performance screenshots here if needed.
