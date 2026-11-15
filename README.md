# Movie recommendation engine

A content-based movie recommender with a **Streamlit** interface. Pick a movie and it returns the five most similar titles with their posters.

![App screenshot](https://github.com/HamzaAbbas0/Netflix_Movie_Recommendation_Systems_Machine_Learning/assets/92590229/c222438b-3ca5-4f2f-9ea1-4b8be037ba34)

## How it works

1. The notebook `nerlix_recommendation_engine_ML.ipynb` cleans the **TMDB 5000** movies and credits datasets and builds one text profile per movie.
2. The profiles are vectorised and a movie-to-movie similarity matrix is computed.
3. The app looks up the selected movie's row in that matrix, sorts by similarity, and returns the top five.
4. Posters are fetched live from the TMDB API.

## Stack

Python · pandas · scikit-learn · Streamlit · TMDB API

## Run it

```bash
pip install streamlit pandas scikit-learn requests
```

1. Run the notebook once to generate `similarity.pkl`. It is too large to store in the repository.
2. Get a free API key from [themoviedb.org](https://www.themoviedb.org/settings/api) and set it as the `TMDB_API_KEY` environment variable.
3. Start the app:

```bash
streamlit run main.py
```

## Files

| File | Purpose |
|---|---|
| `nerlix_recommendation_engine_ML.ipynb` | Data cleaning, feature building, similarity matrix. |
| `main.py` | Streamlit app. |
| `movie_dict.pkl` | Processed movie table used by the app. |
| `tmdb_5000_movies.csv`, `tmdb_5000_credits.csv` | Source data. |

## Author

Hamza Abbas · [LinkedIn](https://www.linkedin.com/in/hamza-abbas-851864229/) · [GitHub](https://github.com/HamzaAbbas0)
