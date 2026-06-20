# House Price Prediction

A beginner-friendly machine learning project that explores a housing dataset, cleans and prepares the data, builds two regression models to predict house prices, and visualizes the key findings.

This was completed as a Week 1 internship project, broken into 5 tasks.

## 📂 Project Structure

```
HousePricePrediction_AdityarajThorat/
├── analysis.ipynb          # Complete notebook — all 5 tasks
├── Housing.csv              # Dataset used
├── summary.pdf / .docx      # 1-page written summary of findings
├── charts/                  # Saved chart images
│   ├── chart1_price_distribution.png
│   ├── chart2_correlation_heatmap.png
│   └── chart3_actual_vs_predicted.png
└── README.md
```

## 📊 Dataset

`Housing.csv` contains **545 house listings** with **13 columns**:

| Column | Description |
|---|---|
| `price` | Sale price (target variable) |
| `area` | Plot area in square feet |
| `bedrooms`, `bathrooms`, `stories` | Counts of rooms/floors |
| `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea` | Yes/No amenities |
| `parking` | Number of parking spaces |
| `furnishingstatus` | Furnished / Semi-furnished / Unfurnished |

## 🛠️ Tasks Completed

1. **Data Loading & Exploration** — loaded the CSV, previewed rows, checked shape and missing values, identified `price` as the target.
2. **Data Cleaning** — handled missing values, removed duplicates, one-hot encoded categorical columns (yes/no fields and `furnishingstatus`).
3. **Model Building** — split data 80/20, trained a **Linear Regression** model and a **Random Forest Regressor**, evaluated both with MAE, RMSE, and R².
4. **Visualization** — price distribution histogram, feature correlation heatmap, and an actual-vs-predicted price scatter plot.
5. **Insights & Summary** — written conclusions on key price drivers, model accuracy, and a real estate business recommendation.

## 📈 Results

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear Regression | ₹970,043 | ₹1,324,507 | **0.653** |
| Random Forest | ₹1,022,560 | ₹1,401,497 | 0.611 |

Linear Regression slightly outperformed Random Forest on this dataset — likely because price scales fairly linearly with features like area and bathrooms, and the dataset (545 rows) is small enough that Random Forest's extra flexibility leads to mild overfitting.

**Top price-driving features:** `area`, `bathrooms`, `airconditioning`, `stories`, `parking`.

## 🧰 Tools & Libraries

- Python
- Pandas, NumPy
- scikit-learn (`LinearRegression`, `RandomForestRegressor`, `train_test_split`, metrics)
- Matplotlib, Seaborn
- Jupyter Notebook

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/HousePricePrediction.git
   cd HousePricePrediction
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
   ```
3. Launch Jupyter and run all cells:
   ```bash
   jupyter notebook analysis.ipynb
   ```

## ✍️ Author

**Adityaraj Thorat**
