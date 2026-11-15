# Movie Recommendation System

A content-based movie recommender with review sentiment analysis, served as a Flask web app. I built this while following an online course.

## How it works

- **Recommendations:** each movie is described by its director, top three actors and genres. `CountVectorizer` and cosine similarity return the ten most similar movies (`main.py`).
- **Review sentiment:** a TF-IDF and Multinomial Naive Bayes model labels user reviews as good or bad (`comment_model.ipynb`, 97.5% accuracy on the test split).
- **Data:** movie metadata up to 2016, TMDb data for 2017 and Wikipedia lists of American films from 2018 to 2022, combined in `data process.ipynb` into `main_data.csv`.
- **Web app:** Flask with jQuery; movie details come from the TMDb API.

## Running it

1. Install the dependencies: `pip install -r requirements.txt`
2. Get a TMDb API key and put it in `static/recommend.js` (`TMDB_API_KEY`). To rerun the data notebook, set the `TMDB_API_KEY` environment variable.
3. Start the app: `python main.py`
