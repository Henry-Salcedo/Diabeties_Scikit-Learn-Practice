# Diabeties_Scikit-Learn-Practice
Reviewing the diabetes dataset within Scikit Learn to practice generating machine learning regression models, reviewing there performance, in addition to determining ways to improve upon there initial run.

## Puropse
  Generating 3 machine learning regression models that use standard data division for the diabetes dataset in Scikit Learn. Then, determine if one of the 3 is better than the others, and if not, determine the pros/cons of the models.

This project's aim was to focus on “Scikit learn” to create machine learning models, spcificly regression models.
The project reads the diabetes dataset that is within “Scikit learn” that contains multiple columns.
The goal is to generate machine learning models and identify which one demonstrates the highest predictive accuracy and effectiveness.
  
Key analyses include:
- Extracted the data (X) and target (y).
- Split the data into 80% training and 20% test_size.
- Created a Linear regression, Random Forest Regressor, and Support Vector Regression (SVR) models.
- Tested their prediction by reviewing Variance, Mean square error, and R^2 scores across the models. Then reviewed the findings.
- Wrote a brief paragraph defining if one of the model was the best performing.

## Class Design
The project can be classified into 5 different areas:

- Creating the data split
- Setting up models
- Prediction scores
- Print out results (Variance, Mean square error, and R^2)
- Reviewed results for the best-performing model

## Class Attributes and Methods

### Data Split

**Attributes:**
- dia.data - Feature data from the dataset
- dia.target - Labels from dataset
- test_size=0.2 - 20% for test set
- random_state= 42 - Seed for reproducibility
  
**Methods:**
- dia = datasets.load_diabetes() - Loads the diabetes dataset
- model_selection.train_test_split() - Splits data into train/test sets

---
### Setting Up Models

**Attributes:**
- LinearRegression()
- RandomForestRegressor(n_estimators=75, random_state=42)
- SVR(kernel='rbf', C=100, gamma=0.1, epsilon=.1)

**Methods:**
- .fit(x_train, y_train) - Trains each model on training data

---
### Predicting Scores
**Attributes:**
- y_pred_linreg - Array of predictions from the Logistic Regression model
- y_pred_forest - Array of predictions from the K-Nearest Neighbors model
- y_pred_svr - Array of predictions from Random Forest model
-   
**Methods:**
-.predict(x_test) - Generates predictions on each test datas model

---
### Results

**Attributes:** / **Methods:**
- explained_variance_score(y_test, y_pred_(linreg, forest, or svr)), Calculated the Explained Variance Score
- mean_squared_error(y_test, y_pred_(linreg, forest, or svr)), Calculated the Mean Squared Error Score.
- r2_score(y_test, y_pred_(linreg, forest, or svr)), Calculated the R^2 Score.

---
## Limitations
- I will slightly limited myself to what I learn in a class related to the project, but will attempt a few things within Scikit-learn.
- In addition to the small limits of class-related, I also limited myself from generating models since such an area has not been discussed (Once more, such a thing is possible now, however, these limits are to test what the library can do).
- Focused solely on using sklearn to establish a better understanding of its usage, and for the current project using regression models. 

## Post Implementation/Thoughts
These are some of the implementation/Thoughts post methods to highlight the areas that I improved and/or discussed upon the initial methods:

- I decided to try using k-fold cross-validation on the 3 models to see if I could improve how each results could change, with the help of numpy.
- Over all after manipulating the number of forest the random forest model did closes the gap and came extremely closes to surpassing the linear model but fell short by a little. Perhaps I could expand upon more ways to affect trees to finally surpass linear.
- Lastly, the k-fold only improved the SVR (Support Vector Regressor) (more details regurding why within notebook), however once again only closed the gap towards linear regression slightly. Review/see if Ridge and Lasso could help to improve the models.
