# House Price Prediction
### Project Overview
Predict real estate prices using regression models.Estimating Real Estate Prices Using Machine Learning ModelsIn recent years, 
the cost of housing has been steadily rising across many countries, making home ownership increasingly difficult for a significant 
portion of the population. Housing affordability has become one of the major social and economic challenges worldwide, 
affecting quality of life, migration patterns, and the financial stability of families. Accurate price prediction models can 
help buyers, investors, developers, and policymakers make more informed decisions.

### Objectives
- Develop accurate machine learning models for house price prediction
- Identify key factors influencing property prices
- Compare multiple regression algorithms
- Provide actionable insights for buyers and investors

### Dataset
Source: Melbourne Housing Market Dataset. 
- Link: https://www.kaggle.com/datasets/anthonypino/melbourne-housing-market

Description:The dataset includes address, Property type, suburb, method of sale, Rooms, price, Real Estate Agent, date of sale, and distance from C.B.D.
Now that there is additional data, including the size of the property, the land area and the municipal area.

- Samples: ~34,000 properties
- Features: 21 attributes
- Target: Price (in AUD)
- Time Period: 2016-2018

### Setup and Usage
#### 1. Download Dataset

Download the **Melbourne Housing Market** dataset from the Kaggle website in the **Melbourne_housing_FULL.csv** file.

`path = kagglehub.dataset_download("anthonypino/melbourne-housing-market")`

`print("Path to dataset files:", path)`

`file_path = os.path.join(path, "Melbourne_housing_FULL.csv")`

`df = pd.read_csv(file_path)`

#### 2. Execute All Cells
Run all cells sequentially to:
- Load and explore the dataset
- Preprocess and clean data
- Perform exploratory data analysis
- Train multiple ML models
- Evaluate and compare results

#### 3. View Results

Generated outputs:
- Cleaned Dataset: Melbourne_housing_CLEANED.csv
- Visualizations: Multiple PNG files with analysis plots

### Methodology
#### 1. Data Preprocessing
- Handled missing values using median/mode imputation
- Removed outliers (±3 standard deviations)
- Encoded categorical variables
- Feature engineering: created new derived features
- Feature scaling using StandardScaler

#### 2. Exploratory Data Analysis
- Statistical summaries and distributions
- Correlation analysis
- Feature relationship visualizations
- Identified key price drivers

#### 3. Model Development
Implemented 4 regression models: 

- Model: |-Linear Regression-|, |-Ridge Regression-|, |-Random Forest-|, |-Gradient Boosting-|.
- Type:  |-Baseline         -|, |-Regularized     -|, |-Ensemble     -|, |-Ensemble         -|

#### 4. Model Evaluation
Metrics used:

- R² Score: Model accuracy (0-1, higher is better)
- RMSE: Root Mean Squared Error (lower is better)
- MAE: Mean Absolute Error (lower is better)

### Results
#### Key Findings
##### Top 5 Price Influencers:
1. Price_per_Room — The main factor in all models is
2. Rooms (number of rooms)
3. Room_to_Bathroom_Ratio
4. Bathroom (number of bathrooms)
5. Distance (distance from the center / CBD)

##### Best Model: Random Forest Regressor
- Highest R² score
- Captures nonlinear dependencies well
- Does not overestimate secondary features compared to linear models

##### Insights
- Price per room is a key cost driver: significantly exceeds all other signs in importance in all models.
- Size and layout are more important than geography: the number of rooms and the ratio of rooms to bathrooms have a stronger effect than latitude/longitude
- Geographical features have a secondary role: Latitude, Longitude, CouncilArea, and Regionname give a minimal contribution.
- Tree-based models and linear models converge on the main point: the top 2 attributes (Price_per_Room and Rooms) are stable in all approaches

### Future Improvements
#### 1. Feature Enhancement
- Include economic indicators (interest rates, inflation)
- Add neighborhood amenities (schools, transport)
- Incorporate seasonal trends

#### 2. Advanced Models
- Deep learning (neural networks)
- XGBoost for better performance
- Ensemble stacking methods

#### 3. Expanded Analysis
- Time series analysis for price trends
- Market segmentation by property type
- Investment ROI predictions

### References
1. Kaggle Melbourne Housing Market Dataset: https://www.kaggle.com/datasets/anthonypino/melbourne-housing-market
2. Scikit-learn Documentation: https://scikit-learn.org/
3. Machine Learning Course of Professor Dr. Abdul Razaque
4. OpenAi assistance
5. Anthropic Claude assistance helped with the documentation

### License
This project is developed for academic purposes as part of a Machine Learning course.

Dataset License: Check Kaggle page
