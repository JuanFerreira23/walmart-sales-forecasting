# Walmart Sales Forecasting

A Machine Learning project for predicting Walmart weekly sales using Exploratory Data Analysis (EDA), Feature Engineering, and Regression models.

---

## 📌 Project Overview

This project aims to predict Walmart's weekly sales using historical sales data, store information, and external economic indicators.

The complete Machine Learning workflow was implemented, including:

- Data Understanding
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis (EDA)
- Model Training
- Model Evaluation
- Model Persistence
- Prediction on New Data

---

## 📂 Dataset

The project uses the **Walmart Sales Forecasting** dataset, composed of three files:

- `train.csv` → Historical weekly sales
- `features.csv` → Economic indicators and promotional information
- `stores.csv` → Store characteristics

The dataset contains information such as:

- Weekly Sales
- Store ID
- Department
- Temperature
- Fuel Price
- CPI
- Unemployment Rate
- Holiday Weeks
- Promotional MarkDowns
- Store Type
- Store Size

---

## 🚀 Technologies Used

- Python 3.12
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Joblib
- Jupyter Notebook

---

## 📁 Project Structure

```text
sales-data-eda/
│
├── data/
│   ├── raw/
│   │   ├── train.csv
│   │   ├── features.csv
│   │   └── stores.csv
│   │
│   └── processed/
│       ├── walmart_processed.csv
│       ├── random_forest_model.pkl
│       └── model_columns.pkl
│
├── images/
│   ├── random_forest_feature_importance.png
│   └── random_forest_real_vs_predicted.png
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data.ipynb
│   └── 03_predict.ipynb
│
├── src/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

## 📊 Exploratory Data Analysis

During the exploratory analysis, the following investigations were performed:

- Dataset overview
- Missing values analysis
- Weekly sales distribution
- Outlier detection
- Monthly sales analysis
- Holiday impact on sales
- Top-performing stores
- Store type comparison
- Store size analysis
- Correlation analysis
- Feature importance

Several visualizations were generated to better understand the data.

---

## ⚙️ Feature Engineering

New features created:

- Year
- Month
- Day
- Quarter
- Week
- DayOfWeek

Data from all datasets were merged into a single processed dataset.

Missing values in promotional variables (`MarkDown1` to `MarkDown5`) were replaced with zero.

Categorical variables were transformed using One-Hot Encoding.

---

## 🤖 Machine Learning Models

Two regression models were evaluated:

### Linear Regression

Performance metrics:

- MAE
- RMSE
- R² Score

---

### Random Forest Regressor

The Random Forest model achieved the best overall performance and was selected as the final model.

The trained model was saved using Joblib for future predictions.

---

## 📈 Model Evaluation

Evaluation metrics used:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

Model performance was also analyzed through:

- Actual vs Predicted plot
- Feature Importance

---

## 💾 Saved Model

The following files are generated after training:

```text
random_forest_model.pkl
model_columns.pkl
```

These files are loaded by the prediction notebook to perform inference on new data.

---

## 🔮 Example Prediction

After loading the trained model, a prediction can be made using new store information.

Example output:

```text
Predicted Weekly Sales:
$158,852.76
```

---

## 📷 Generated Visualizations

The project generates several visualizations, including:

- Weekly Sales Distribution
- Boxplot of Weekly Sales
- Monthly Sales
- Average Monthly Sales
- Holiday vs Non-Holiday Sales
- Top Stores by Sales
- Sales by Store Type
- Correlation Heatmap
- Feature Importance
- Actual vs Predicted Values

---

## ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/your-username/walmart-sales-forecasting.git
```

Navigate to the project folder:

```bash
cd walmart-sales-forecasting
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Run the notebooks in the following order:

1. `01_data_understanding.ipynb`
2. `02_data.ipynb`
3. `03_predict.ipynb`

---

## 📌 Future Improvements

- Hyperparameter tuning
- Cross-validation
- XGBoost implementation
- LightGBM implementation
- Model deployment with FastAPI
- Interactive dashboard using Streamlit

---

## 👨‍💻 Author

**Juan Rodrigues Ferreira**

Computer Science Student

---

## 📄 License

This project is licensed under the MIT License.