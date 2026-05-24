
Economic Indicators of Real Estate: A Regression Analysis



Project Objective
The primary goal of this project was to analyze how specific economic indicators—specifically Median Income—influence housing prices in California. Using a machine learning approach, we developed a predictive model to quantify this relationship and visualize the market trend.


Dataset Acquisition
We utilized the California Housing Dataset (sourced via sklearn.datasets). This dataset contains 20,640 observations with features such as housing age, average rooms, population, and the target variable, Price.



Data Inspection and Cleaning
Before building the model, we performed a thorough data audit:

.  Missing Value Analysis: We checked for null entries to ensure data integrity. In    this specific dataset, the data was pre-cleaned, but we established a workflow to handle missing values using Mean Imputation if necessary.

.  Duplicate Removal: We scanned the dataset for redundant rows to prevent the model from being biased toward repeated data points.



Exploratory Data Analysis (EDA)
To understand the relationships between variables, we conducted a visual correlation study:

Correlation Heatmap: Using the Seaborn library, we generated a heatmap of the correlation matrix. This allowed us to mathematically identify that Median Income had the strongest positive correlation with house prices (approximately 0.69)


Data Preprocessing
.   Feature Selection: Based on our EDA, we selected 'Median Income' as our independent variable (X) and 'Price' as our dependent variable (y).
.   Train-Test Split: To evaluate the model's true performance, we split the data into a Training Set (80%) to teach the model and a Testing Set (20%) to validate its predictions.



Linear Regression Modeling
We implemented a Simple Linear Regression algorithm. 
The model calculated the "Line of Best Fit" by determining the optimal slope (m) and intercept (c) to minimize prediction errors.
Calculated Slope: ~0.419 (indicating that as income rises, price tends to rise proportionally).

 
 
Performance Evaluation
We used two key statistical metrics to judge our model:
.   Mean Squared Error (MSE): Used to measure the average squared difference between actual prices and predicted prices.
.   R-Squared (R^2) Score: This score (approx. 0.47) confirmed that nearly half of the variation in house prices can be explained solely by the income level of the residents.


Visualization of Results
The final stage involved plotting the Regression Line against the actual test data. This visualization clearly demonstrates the linear trend: as the economic indicator (Income) moves right, the predicted House Value moves up.


