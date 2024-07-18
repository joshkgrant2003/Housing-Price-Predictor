# Housing Price Predictor

## Project Overview
This project aims to predict housing prices based on various features such as location, age, number of rooms, population, households, median income, and proximity to the ocean. The dataset used contains several attributes for houses in California.

## Dataset
The dataset includes the following features:
1. longitude: A measure of how far west a house is; a higher value is farther west
2. latitude: A measure of how far north a house is; a higher value is farther north
3. housingMedianAge: Median age of a house within a block; a lower number is a newer building
4. totalRooms: Total number of rooms within a block
5. totalBedrooms: Total number of bedrooms within a block
6. population: Total number of people residing within a block
7. households: Total number of households, a group of people residing within a home unit, for a block
8. medianIncome: Median income for households within a block of houses (measured in tens of thousands of US Dollars)
9. medianHouseValue: Median house value for households within a block (measured in US Dollars)
10. oceanProximity: Location of the house w.r.t ocean/sea

## Data Preprocessing
1. **Handling Missing Values**: Dropped rows with NaN values.
2. **Encoding Categorical Data**: One-hot encoded the `ocean_proximity` column.
3. **Feature Transformation**: Applied logarithmic transformation to right-skewed features (`total_rooms`, `total_bedrooms`, `population`, `households`).
4. **Feature Engineering**: Created new features:
   - `bedroom_ratio`: Ratio of bedrooms to total rooms.
   - `household_rooms`: Ratio of total rooms to households.

## Data Visualization
- **Histograms**: Visualized distributions of features.
- **Heatmap**: Visualized correlation between features and the target variable.
- **Scatter Plot**: Visualized house values based on geographical coordinates.

## Models
### Linear Regression
- Scaled features using `StandardScaler`.
- Trained a Linear Regression model.
- Evaluated the model performance.

### Random Forest Regressor
- Trained a Random Forest model.
- Evaluated the model performance.
- Performed hyperparameter tuning using `GridSearchCV` to improve model performance.
 
## Conclusion
- The project demonstrates the process of data preprocessing, feature engineering, model training, and evaluation to predict housing prices. The tuned Random Forest model showed improved performance compared to the basic models.

## Acknowledgments
- This project was completed as part of a learning exercise. The dataset is publicly available at [kaggle.com](https://www.kaggle.com/datasets/camnugent/california-housing-prices?resource=download) and was used for educational purposes.
