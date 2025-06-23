# 🏃‍♀️ Fitness Tracker App – Calorie & Exercise Data Analysis with Streamlit

This project is a **fitness tracker web application** developed using Python, Streamlit, and machine learning. It predicts **calories burned during exercise**, visualizes user data, and helps individuals track and understand their physical activity metrics.

---

##  Project Objective

To build an end-to-end fitness tracker system that:
- Takes user input for physical metrics and exercise duration
- Predicts calories burned using a trained machine learning model
- Visualizes workout trends and statistics
- Provides a lightweight web app interface via Streamlit

---

##  Project Structure

| File | Description |
|------|-------------|
| `fitness_tracker.ipynb` | Jupyter notebook containing data cleaning, EDA, and model training |
| `app.py` | Streamlit application script |
| `calories.csv`, `exercise.csv` | Datasets used for model training and merging |
| `README.md` | Project documentation (this file) |

---

##  Dataset Information

- **calories.csv**:
  - Columns: `User_ID`, `Gender`, `Age`, `Height`, `Weight`, `Calories`
- **exercise.csv**:
  - Columns: `User_ID`, `Duration`, `Heart_Rate`, `Body_Temp`

These datasets are merged on `User_ID` for training a regression model to predict calories burned.

---

##  Exploratory Data Analysis (EDA)

Key EDA insights:
- Positive correlation between heart rate and calories burned
- Body temperature and duration also impact energy expenditure
- Gender-based and age-based calorie burn comparisons were visualized

Visualizations include:
- Heatmaps
- Pairplots
- Distribution plots

---

##  Model Development

- Used **Random Forest Regressor** for calorie prediction
- Achieved high R² score (~0.98)
- Hyperparameter tuning applied using `GridSearchCV`

```python
# Features used:
['Age', 'Height', 'Weight', 'Duration', 'Heart_Rate', 'Body_Temp']
