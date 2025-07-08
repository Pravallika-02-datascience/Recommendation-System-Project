🔥 Project Title
🎥 Anime Recommendation System using Machine Learning & Cosine Similarity

🧾 Executive Summary
This project builds a robust Content-Based Recommender System for anime using Python and Scikit-learn. By leveraging metadata such as genres, type, user ratings, number of episodes, and popularity, the system computes cosine similarity across all entries in the dataset to deliver highly relevant, personalized recommendations to the user.

It’s a modular, scalable system that can be deployed as a backend engine or integrated into interactive web applications using frameworks like Streamlit or Flask.


🧠 Motivation
Recommendation systems are the backbone of digital platforms — from Netflix to Spotify — enhancing user experience by suggesting what they’re most likely to engage with. This project aims to:

Simulate a Netflix-style recommender system for anime

Explore and apply feature engineering and similarity-based search

Lay the foundation for hybrid models (collaborative + content-based)

🎯 Objectives
Build a content-based filtering system from scratch

Engineer meaningful features from genre and numeric data

Generate top-N anime recommendations with high precision

Evaluate recommendation quality using precision/recall

Create a ready-to-deploy modular pipeline

📊 Dataset Description
Source: Kaggle Anime Recommendation Database

Total Entries: 11,830+

Key Attributes:

name: Anime title

genre: Comma-separated list of genres (e.g., "Action, Shounen, Supernatural")

type: Format (TV, Movie, OVA, etc.)

episodes: Total number of episodes

rating: Average user rating

members: Number of users who added it to their list

🛠 Feature Engineering:

| Feature                         | Technique Used  | Description                             |
| ------------------------------- | --------------- | --------------------------------------- |
| `genre`                         | CountVectorizer | Converts genres to multi-hot encoding   |
| `type`                          | OneHotEncoder   | Converts type to binary flags (TV, OVA) |
| `rating`, `episodes`, `members` | StandardScaler  | Normalized to z-score scale             |

🧠 Recommendation Algorithm
🔗 Cosine Similarity:
Cosine similarity is used to compute the angle between the feature vectors of two anime, indicating their closeness.

🧮 Top-N Recommendation Function:
For a given anime title:

Get its vector representation

Compute similarity with all others

Filter by minimum similarity threshold (e.g., 0.2)

Sort and return top N titles

📈 Evaluation Strategy
✅ Evaluation Logic:
Hold out 20% of the data for testing

For each anime in test:

Recommend top-k similar titles

Check if at least one recommended anime matches its type

Compute classification-style metrics (binary hit/miss)

📊 Results:
| Metric    | Score     |
| --------- | --------- |
| Precision | **1.000** |
| Recall    | **0.997** |
| F1-score  | **0.998** |


🚀 Future Scope
Hybrid Recommender: Combine with collaborative filtering for user-based insights

Fast Search: Use Approximate Nearest Neighbors (e.g., FAISS, Annoy)

Streamlit Web App: Turn it into a public-facing recommender portal

User Login System: Save preferences, ratings, and personalization

Visualization Dashboard: Show genre trends, recommendation maps, etc.

🧪 Tech Stack
| Category         | Tools Used                         |
| ---------------- | ---------------------------------- |
| Programming      | Python                             |
| Data Wrangling   | pandas, numpy                      |
| Machine Learning | scikit-learn                       |
| Text Processing  | CountVectorizer                    |
| Similarity       | cosine\_similarity                 |
| Evaluation       | Precision, Recall, F1 from sklearn |
| Notebook         | Jupyter                            |

