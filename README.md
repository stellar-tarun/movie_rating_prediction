# movie_rating_prediction

Movie Rating Prediction Using Regression
This project focuses on predicting IMDB ratings for Indian movies by leveraging various movie metadata. Machine learning regression models are employed to achieve this objective.

Objective
The primary goal of this project is to build a robust model capable of estimating movie ratings based on features such as Genre, Year, Duration, Director, and Actors.

Techniques Used
Data Cleaning & Preprocessing: Handling missing values, converting data types, and standardizing formats.

One-Hot Encoding: Converting categorical features into a numerical format suitable for machine learning models.

Linear Regression: A fundamental regression algorithm used as a baseline model.

Decision Tree Regression: A non-linear regression algorithm capable of capturing complex relationships in the data.

RMSE (Root Mean Squared Error) & MAE (Mean Absolute Error) evaluation: Metrics used to assess the performance of the regression models.

Dataset
The dataset used in this project is imdb_movies.csv, which contains information about Indian movies including their names, release years, durations, genres, IMDB ratings, number of votes, and primary cast and crew.

Installation
To run this project, you'll need to have Python installed along with the following libraries. You can install them using pip:

Bash

pip install pandas numpy matplotlib seaborn scikit-learn
Usage
Clone the repository:

Bash

git clone https://github.com/your-username/movie-rating-prediction.git
cd movie-rating-prediction
Place the dataset:
Ensure the imdb_movies.csv file is in the root directory of the cloned repository.

Run the Jupyter Notebook:
Open the movie_rating_prediction.ipynb notebook using Jupyter Lab or Jupyter Notebook and run all cells.

Bash

jupyter notebook movie_rating_prediction.ipynb
The notebook will guide you through the data loading, cleaning, preprocessing, model training, and evaluation steps.

Project Structure
movie_rating_prediction.ipynb: The main Jupyter Notebook containing all the code for data analysis, model building, and evaluation.

imdb_movies.csv: The dataset used for movie rating prediction.

README.md: This README file.

Data Cleaning and Preprocessing Steps
The following steps were performed to prepare the data for modeling:

Load Data: The imdb_movies.csv dataset was loaded using pandas, specifying encoding="latin1" to handle special characters.

Handle Missing Ratings: Rows with missing Rating values were dropped as they are essential for the prediction task.

Clean Year Column: Year values were extracted using a regular expression to get the 4-digit year and converted to float type.

Clean Duration Column: The "min" suffix was removed from the Duration column, and values were converted to numeric (float) type.

Clean Votes Column: Commas were removed from the Votes column, and values were converted to numeric type.

Impute Missing Numeric Values: Missing values in Year, Duration, and Votes were filled with their respective median values.

Impute Missing Categorical Values: Missing values in Director, Actor 1, Actor 2, Actor 3, and Genre were filled with "Unknown".

Extract Main_Genre: A new column Main_Genre was created by taking the first genre listed in the Genre column.

One-Hot Encoding: Categorical features like Main_Genre, Director_simple (top directors, others grouped), and Actor1_simple (top actors, others grouped) were converted into numerical format using one-hot encoding.

Model Training and Evaluation
Two regression models were trained and evaluated:

Linear Regression:

Trained on the preprocessed features (Year, Duration, Votes, one-hot encoded Genre, Director, and Actor 1).

RMSE: 1.23.

MAE: 0.97.

Decision Tree Regressor:

Trained on the same preprocessed features.

RMSE: 1.54.

MAE: 1.16.

Results
The Linear Regression model demonstrated better performance with lower RMSE and MAE values compared to the Decision Tree Regressor. This indicates that the Linear Regression model generalizes more reliably for this movie rating prediction task.

A scatter plot visualizing the actual vs. predicted movie ratings for the Linear Regression model is generated in the notebook, showing the spread of predictions against the true ratings.

Contributing
Feel free to fork this repository, make improvements, and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.
