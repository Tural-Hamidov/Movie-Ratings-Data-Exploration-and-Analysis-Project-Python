# Movie-Ratings-Data-Exploration-and-Analysis-Project (Python)
Polars-based data exploration and analysis of movie ratings, focused on user behavior, genre patterns, tag usage, and rating dynamics.
# 🎬 Movie Ratings Data Exploration and Analysis Project (Python)

A structured exploratory data analysis project developed in Python. The project focuses on examining movie ratings, genre-based differences, user behavior, tag activity, and rating dynamics.

---

## 📌 Project Overview

This project explores, cleans, and analyzes a relational movie ratings dataset using **Polars**.  
The workflow is built around two main principles: first, validating the structure of the data, and then generating analytical insights.

---

## 📂 Dataset

The project uses three related tables:

- **movies.csv** — movie information (`movieId`, `title`, `genres`)
- **ratings.csv** — user ratings (`userId`, `movieId`, `rating`, `timestamp`)
- **tags.csv** — user-generated tags (`userId`, `movieId`, `tag`, `timestamp`)

Together, these tables make it possible to analyze:

- movie popularity
- user rating behavior
- genre-based differences
- tag usage patterns

---

## 🔍 Data Inspection and Validation

Each table was initially inspected using the following methods:

- `.head()`
- `.describe()`
- `.schema()`

### Main validation results

- All three datasets were loaded successfully
- Column types were appropriate for analysis
- No missing values were detected
- No fully duplicated rows were found
- `rating` values were confirmed to be within the range of **0.5 to 5.0**

---

## 📈 Main Findings

### Rating behavior
- The most frequently given rating was **4.0**
- **3.0** and **5.0** were also observed at high frequency
- Lower ratings appeared less often

This suggests that users generally tend to give **medium to high ratings**.

### User activity
- Minimum number of ratings per user: **20**
- Maximum number of ratings per user: **2698**
- Average number of ratings per user: **165.3**

Top 5 most active users:
- **414**
- **599**
- **474**
- **448**
- **274**

This shows that user activity is **not evenly distributed**. Some users submitted far more ratings than others.

### Genre-level findings
- Total number of unique genres: **20**
- Most common genres:
  - **Drama** — 4361
  - **Comedy** — 3756
  - **Thriller** — 1894
  - **Action** — 1828
  - **Romance** — 1596

Genres with the highest average ratings:
- **Film-Noir**
- **War**
- **Documentary**

This indicates that genre frequency and genre evaluation are not the same thing. Some genres are more common, while others receive higher average ratings.

### Movie-level findings
- **3446** movies received only **1** rating
- **1298** movies received **2** ratings
- **800** movies received **3** ratings

This shows that most movies in the dataset received only a small number of ratings, while only a limited number of movies attracted high attention.

Among the most frequently rated movies:
- **Forrest Gump (1994)**
- **The Shawshank Redemption (1994)**
- **Pulp Fiction (1994)**
- **The Silence of the Lambs (1991)**
- **The Matrix (1999)**

Among the highest average-rated movies with at least 10 ratings:
- **Secrets & Lies (1996)**
- **Guess Who’s Coming to Dinner**
- **Paths of Glory**
- **A Streetcar Named Desire**

### Tag usage
- Average number of tags per movie: **2.34**
- Minimum number of tags per movie: **1**
- Maximum number of tags per movie: **181**

Most frequently used tags:
- **In Netflix queue**
- **atmospheric**
- **thought-provoking**
- **superhero**
- **funny**

This suggests that tag usage is uneven, and some tags are used much more frequently than others.

### Re-rating behavior
- Re-rating proportion was calculated at the user level
- In the displayed results, this value was observed as **0.0**

### Correlation result
- Correlation between the number of ratings a movie receives and its average rating: **0.127**

This value indicates a **weak positive relationship**. In other words, movies with more ratings tend to have slightly higher average ratings, but the relationship is not strong.

---

## 📊 Visual Analysis

A **scatter plot** was created to show the relationship between the number of ratings a movie receives and its average rating.

This visualization supports the correlation result and shows that the relationship is positive but weak.

---

## ✅ Final Conclusion

The analysis led to the following overall conclusions:

- users tend to give **medium to high ratings**
- user activity is **not evenly distributed**
- **Drama** and **Comedy** dominate the dataset in terms of frequency
- genres such as **Film-Noir** and **War** receive higher average ratings
- most movies receive only a small number of ratings
- tag usage is concentrated around a few recurring expressions
- there is only a **weak relationship** between movie popularity and average rating

Overall, this project demonstrates that **Polars** can be used effectively to perform fast, structured, and readable exploratory data analysis on a relational dataset.

---

