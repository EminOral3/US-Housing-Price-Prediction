# 🏠 US Apartment Rental Price Prediction (DSL Project)

This project was developed in the **Data Science and Learning (DSL)** course at Politecnico di Torino. The goal is to predict monthly rental prices of apartments in the United States with minimal error by analyzing listing features.

---

## 📋 Project Overview and Objective

The real estate market is complex, involving both structured data (e.g., number of rooms, square footage, location) and unstructured data (e.g., listing descriptions, amenities). In this project:

- Large-scale dataset preprocessing was performed
- Meaningful insights were extracted from text data using NLP techniques
- Advanced regression models achieved a **169.20 MAE (Mean Absolute Error)**

---

## 🛠️ Technologies and Tools

- **Language:** Python 3.x  
- **Data Processing:** Pandas, NumPy  
- **Machine Learning:** LightGBM, Scikit-learn  
- **Text Analysis (NLP):** TfidfVectorizer  
- **Visualization:** Matplotlib, Seaborn  
- **Mathematical Operations:** SciPy (Sparse matrices), NumPy (Log transformations)

---

## 🧪 Methodology

### 1. Data Preprocessing

- **Log Transformation:**  
  Applied `log1p` transformation to reduce variance in rental prices.

- **Missing Value Handling:**  
  - Numerical features: filled with median  
  - Categorical features: filled with most frequent value  

- **Outlier Analysis:**  
  Conducted to improve model generalization.

---

### 2. Feature Engineering

- **Text Mining (TF-IDF):**  
  `title`, `body`, and `amenities` columns were vectorized using TF-IDF to capture key terms like *"luxury"*, *"renovated"*, *"pool"*.

- **Categorical Encoding:**  
  Applied `OneHotEncoder` to convert categorical variables into numeric format.

---

### 3. Modeling: LightGBM

LightGBM was selected for its balance between speed and performance.

- Hyperparameter tuning performed using:
  - `RandomizedSearchCV`
  - **3-fold Cross Validation**

---

## 📊 Results

### Model Performance

- **Validation MAE:** `169.20 USD`

Key findings:

- **Square footage (square_feet)**  
- **Location (latitude/longitude)**  

are the most influential features affecting rental prices.

---

### Data Visualization

> Note: You can generate and insert these visuals by running the provided `.py` scripts.

- Rental Price Distribution (Histogram)
- Correlation Matrix

---

## 💾 Dataset Access and Setup

Due to size limitations, the dataset is hosted externally (Google Drive).

### Step 1: Download Data

Download the following files from:

`(https://drive.google.com/drive/folders/1ZA5tq3axuyfVS1lWPYu9G4THFnV8BoKH?usp=drive_link)`

- `development.csv`
- `evaluation.csv`

Place the downloaded files directly in the project's root directory (the same folder as dsl_project_final.py).

---

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Step 3: Run the Project

```bash
python dsl_project_final.py
```

---

## 📂 Project Structure

```
data/                      # Dataset (user must add)
notebooks/                 # EDA and visualization
dsl_project_final.py       # Main training & prediction script
DSL Report.pdf             # Academic report
housing_predictions.csv    # Model output
```

---

## ✍️ Authors

- Alican Akkiprik - s349610@studenti.polito.it  
- Muhammed Emin Oral - s343124@studenti.polito.it  

**Politecnico di Torino**
