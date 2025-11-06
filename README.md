# 🎬 Movie Recommendation System (Python CLI)

A command-line movie recommendation tool that uses collaborative filtering and cosine similarity to predict movies a user may like—based on real user ratings from a provided CSV file.

---

## ✨ Features

- **Loads a ratings CSV** (user, movie, rating) and builds a pivot table
- **Computes user-user cosine similarity**
- **Suggests movie recommendations for any user**
- **Avoids recommending movies the user already rated**
- **Ranking: Shows top matches with predicted ratings**
- **Easy-to-use CLI with clear prompts**

---

## 🚀 How to Use

1. **Place `movie_ratings.csv` and `movie.py` in the same folder**

2. **Install the required libraries:**
    ```
    pip install pandas scikit-learn
    ```
3. **Run in terminal:**
    ```
    python movie.py
    ```

4. **At the prompt:**
    - Enter the user ID for whom you want recommendations
    - Script prints out a list of suggested movies with predicted scores

---

## 🧑‍💻 What the Code Does

- Loads the CSV (`movie_ratings.csv`)
- Builds a user-movie matrix (rows: users, columns: movies, values: ratings)
- Computes similarity with `cosine_similarity` from sklearn
- Finds the most similar users for a selected user
- Recommends movies that similar users liked but the current user hasn't rated
- Outputs the top recommendations, sorted by predicted rating

---

## 🗂️ Example Input Format (`movie_ratings.csv`)

| user | movie          | rating |
|------|---------------|--------|
| 1    | The Matrix    | 5      |
| 2    | Toy Story     | 4      |
| 1    | Titanic       | 3      |
| ...  | ...           | ...    |

---

## 🏆 Example Output

Welcome to the Movie Recommendation System!
Enter the user ID for recommendations: 4

Recommendations for User 4:
Inception 4.84
The Matrix 4.30
Titanic 4.10

---

## 📄 License

MIT License — free for learning, teaching, and tinkering.

---

A great beginner Python/data science project to learn about recommender systems, data wrangling, and collaborative filtering!
