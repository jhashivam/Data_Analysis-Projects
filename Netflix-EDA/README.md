#  NETFLIX Exploration Data Analysis & Visualization

Netflix is one of the most popular media and video streaming platforms. They have over 10000 movies or tv shows available on their platform, as of mid-2021, they have over 222M Subscribers globally. This tabular dataset consists of listings of all the movies and tv shows available on Netflix, along with details such as - cast, directors, ratings, release year, duration, etc.

## Business Problem

Analyze the data and generate insights that could help Netflix ijn deciding which type of shows/movies to produce and how they can grow the business in different countries


The dataset provided to you consists of a list of all the TV shows/movies available on Netflix:

**  Show_id: Unique ID for every Movie / Tv Show
    Type: Identifier - A Movie or TV Show
    Title: Title of the Movie / Tv Show
    Director: Director of the Movie
    Cast: Actors involved in the movie/show
    Country: Country where the movie/show was produced
    Date_added: Date it was added on Netflix
    Release_year: Actual Release year of the movie/show
    Rating: TV Rating of the movie/show
    Duration: Total Duration - in minutes or number of seasons
    Listed_in: Genre
    Description: The summary description**

## Data and Notebook for Analysis:

1. Data used for analysis - netflix.csv
2. Colab notebook - Netflix_Data_Analysis.ipynb


Data Visualization :

1. we will import relevant libraries to load and explore the dataset. 
    - For this, we imported  numpy, pandas for numerical computations and analysis and matplotlib, seaborn for visualization.
    - The dataset provided to us consists of a list of all the TV shows/movies available on Netflix
2. We will check how many entries in our dataset are null/blank and then accordingly clean our dataset as these are the initial steps of our data preprocessing. therefor we plot a heatmap of the null values to visualize what all records are null.
3. dataset is clean except for ‘director’, ‘cast’ and ‘country’ columns. 
4. Since we need to provide insights aiming to findout the business in different countries, we have to impute the values in ‘country’ column. We will choose to drop the other two columns as they have a lot of missing values. Now let’s explore the distribution of number of TV Shows and Movies present in Netflix.
5. We can visually conclude that our distribution is skewed relative to the type of content present on the platform and the data is unequal for both the categories of content we want to provide insights for. To avoid any bias in our analysis and results, we will divide the data into two categories based on their type (i.e.TV Show and Movie) and proceed further keeping our methodology same for both the categories and deducing possible measures to achieve our aim for each category.
6. data contains a variety of genres as mentioned in the ‘Listed_in’ column. we will pick the top 10 genres for the content provided in the data and drill deeper into them to get insights enabling us to filter out the genres our users are interested in. We will therefore plot a graph to find out what are the top genres of the content present in Netflix.

Data Pre-processing: 

1. We will split our data into two categories on the basis of their type (i.e TV Show or Movie). Also we drop the columns for director and cast from the data.
2. Next step is to impute the empty values in our data for 'country'. 
3. Since we cannot drop this column as our aim is to increase the business in different countries. we will proceed with forward filling of imputation. In upcoming revisions, we will train a model to predict the null values for country using the filled records as our training sample and predicting the values for our empty records.
4. We will also now proceed with imputing other missing values in the records of the data. Part-1 of the data (i.e. with type as Movie) contains two records where the ratings are null. 
5. Therea are more records with empty values in the date_added column were present but we will drop these records as they are not relevant for our analysis much.
6. Filtered top 10 countries with maximum content produced
7. filtered top 10 genres with maximum content produced
8. Filtered for the data for top 10 countries (United States', 'Japan', 'Nigeria', 'France', 'United Kingdom','India', 'Mexico', 'Egypt', 'Canada', 'Spain')

