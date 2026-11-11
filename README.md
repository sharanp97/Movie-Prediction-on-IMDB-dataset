# Movie-Prediction-on-IMDB-dataset
This Python script implements an end-to-end Machine Learning pipeline using scikit-learn to predict IMDb movie ratings based on features like runtime, vote count, release year, primary genre, and content certificate.Using the IMDb Top 250 Movies dataset from your active Jupyter Notebook session, it cleans the data, engineers features, trains a Random Forest Regressor, evaluates model performance, and predicts the rating for a given movie.

What the Code DoesData Preprocessing & Normalization:Standardizes column names to lowercase with underscores to ensure compatibility.Extracts the primary genre from comma-separated genre lists.Selects key predictive features: runtime, votes, year, primary_genre, and certificate.

Pipeline Construction (scikit-learn):Numeric Features (runtime, votes, year): Imputes missing values using the median and standardizes features using StandardScaler.Categorical Features (primary_genre, certificate): Imputes missing values with the most frequent category and encodes them using OneHotEncoder.

Model Training & Evaluation:Splits the data into 80% training and 20% testing sets.Trains a RandomForestRegressor with 300 estimators (n_estimators=300) and parallel processing enabled (n_jobs=-1).Evaluates performance using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and the $R^2$ score.

Inference / Prediction:Demonstrates how to pass new movie metadata (e.g., matching The Shawshank Redemption) into the trained pipeline to predict its IMDb rating.
