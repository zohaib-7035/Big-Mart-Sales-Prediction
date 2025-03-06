# Big Mart Sales Prediction

## Overview
This project aims to predict sales for different outlets of Big Mart using **machine learning** techniques. The dataset contains information about various products and store attributes, and we use **XGBoost Regressor** to model the sales predictions.

## Dataset
The dataset is loaded from `Train.csv` and contains the following key features:
- `Item_Identifier`: Unique ID for each product
- `Item_Weight`: Weight of the product
- `Item_Fat_Content`: Fat content of the product
- `Item_Visibility`: Visibility of the product in-store
- `Item_Type`: Category of the product
- `Item_MRP`: Maximum Retail Price
- `Outlet_Identifier`: Unique store ID
- `Outlet_Size`: Size of the store (Small/Medium/Large)
- `Outlet_Location_Type`: Location of the store
- `Outlet_Type`: Type of store (Grocery, Supermarket, etc.)
- `Item_Outlet_Sales`: Target variable (Sales value)

## Data Preprocessing
- Handling **missing values** in `Item_Weight` (filled with mean)
- Imputing missing values in `Outlet_Size` using **mode based on `Outlet_Type`**
- Data visualization using **Seaborn & Matplotlib**
- Encoding categorical variables using **Label Encoding**

## Exploratory Data Analysis (EDA)
We used **Seaborn** to visualize different distributions:
- **Histograms** for `Item_Weight`, `Item_Visibility`, `Item_MRP`, `Item_Outlet_Sales`
- **Count plots** for categorical variables like `Outlet_Establishment_Year`, `Item_Fat_Content`, `Item_Type`, and `Outlet_Size`

## Model Training
We use **XGBoost Regressor**, a powerful gradient boosting model, to predict `Item_Outlet_Sales`.

### Steps:
1. Split dataset into **training (80%)** and **testing (20%)** sets.
2. Train **XGBoost Regressor** model.
3. Evaluate performance using **R² score**:
   - Training set: `r2_train`
   - Testing set: `r2_test`

## Results
- The model is evaluated using **R Squared (R²) Score**.
- The closer R² is to `1`, the better the model's performance.

## Technologies Used
- **Python** (NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn, XGBoost)

## Future Improvements
- Tune hyperparameters for better accuracy
- Try other models like Random Forest or Deep Learning
- Perform feature engineering for better insights

## Contributing
Feel free to fork the repository and submit pull requests!

