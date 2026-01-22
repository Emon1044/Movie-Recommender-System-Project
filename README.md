# Movie Recommender System 🎬

This is a **Content-Based Movie Recommender System** built using Python. The system analyzes a dataset of 5,000 movies to suggest the most similar films based on a user's preference.

## 🚀 How it Works
The recommender system works by creating a "tags" profile for every movie. It processes metadata such as:
* **Genres** (e.g., Action, Sci-Fi)
* **Keywords** (e.g., space, futuristic)
* **Cast** (Top 3 actors)
* **Crew** (Director)
* **Overview** (Movie plot summary)

It then converts these text tags into vectors using **Bag of Words (CountVectorizer)** and calculates the **Cosine Similarity** between movies to find the closest matches.

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** * `Pandas` & `NumPy` (Data Manipulation)
    * `Scikit-learn` (Vectorization & Similarity)
    * `NLTK` (PorterStemmer for Text Preprocessing)
    * `Ast` (Safe evaluation of literal strings)
    * `Pickle` (Model Deployment)

## 📊 Dataset
The project uses the **TMDB 5000 Movie Dataset**, which includes two files:
1. `tmdb_5000_movies.csv`
2. `tmdb_5000_credits.csv`

## ⚙️ Features & Workflow
1.  **Data Preprocessing:** Merging datasets and handling missing values.
2.  **Feature Extraction:** Extracting genres, keywords, and director names from complex JSON-like strings.
3.  **Text Cleaning:** Removing spaces between words (to treat "James Cameron" as a single entity "JamesCameron") and converting everything to lowercase.
4.  **Stemming:** Reducing words to their root form (e.g., "loving" -> "love").
5.  **Vectorization:** Transforming the "tags" column into a 5,000-dimensional vector space.
6.  **Similarity Engine:** Using Cosine Similarity to measure the distance between movie vectors.

## 🖥️ Usage
To get recommendations, simply call the `recommend()` function with a movie title:

```python
recommend('Iron Man')
