# Global-Temperature-
Climate change has become one of the most critical issues of our time, and understanding long-term temperature patterns is essential for analyzing how the planet is warming. This project focuses on exploring global, Northern Hemisphere, Southern Hemisphere, and zonal temperature datasets collected over more than a century. The goal is to clean, merge, and analyze these datasets to uncover meaningful trends and build predictive models that estimate future temperature anomalies.
Through data cleaning, exploratory data analysis (EDA), visualization, and machine learning models such as Linear Regression and Random Forest, the report demonstrates a full end-to-end Data Science workflow. The findings highlight clear patterns of rising global temperature anomalies and provide insights into the historical and predicted behavior of Earth’s climate.

This project analyzes long term temperature anomalies using four datasets:
Global temperatures
Northern Hemisphere temperatures
Southern Hemisphere temperatures
Zonal annual temperatures

The goal is to clean and merge the datasets, explore historical climate trends, and build two prediction models:
1-Linear Regression.
2-Random Forest Regressor.

The project walks through a full Data Science workflow: preprocessing, EDA, visualization, modeling, and evaluation.
📂 Project Structure
1-global_temps.xlsx
2-nh_temps.xlsx
3-sh_temps.xlsx
4-zonann_temps.xlsx
5-project_code.ipynb
6-README.md

How to Run the Code ? 
Upload the four dataset files into your runtime (Colab or local Jupyter).
Install the required libraries if they aren’t installed:
pip install pandas numpy matplotlib seaborn scikit-learn
Run the code cells in order. The flow is:
1. Import Libraries
Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn.
2. Load the Four Excel Files
df1 = pd.read_excel('global_temps.xlsx')
df2 = pd.read_excel('nh_temps.xlsx')
df3 = pd.read_excel('sh_temps.xlsx')
df4 = pd.read_excel('zonann_temps.xlsx')
3. Clean Missing Values
df1 = df1.ffill()
df2 = df2.ffill()
df3 = df3.ffill()
df4 = df4.ffill()
4. Merge the Datasets
df = df1.merge(df2, on='Year', suffixes=('_global', '_nh'))
df = df.merge(df3, on='Year', suffixes=('', '_sh'))
df = df.merge(df4, on='Year', suffixes=('', '_zon'))
5. Prepare EDA Dataset
We focus on global anomalies:
Temp = J-D_global
6. Run the Linear Regression Model
7. Run the Random Forest Regression Model
8. Compare Both Models
Using:
R² score
RMSE
9. Display Visualizations
Historical trends
Rolling averages
Actual vs Predicted
RF vs LR trendlines


Key Features
Full data cleaning pipeline
Merged multi-source climate dataset
EDA: trends, outliers, anomaly years
Two ML models and performance comparison
Visual interpretation of predictions
