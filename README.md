# 🎬 Movie Recommendation System
This project is a **content-based movie recommendation system** built using **Streamlit**, which suggests similar movies based on a selected title. It utilizes movie metadata and similarity scores to recommend the top 5 most relevant movies along with their posters fetched from the **TMDB API**.

## 🚀 Demo
> A user selects a movie, and the app displays 5 recommended movies with posters, using real-time data from The Movie Database (TMDB).
## 🧠 How It Works

1. Load movie data and similarity matrix (precomputed and pickled).
2. Let the user select a movie via Streamlit UI.
3. On clicking "Show Recommendation":
   - Find the movie index.
   - Sort movies by similarity score.
   - Fetch posters via TMDB API.
4. Display top 5 movie titles and posters side-by-side.

## 🛠️ Technologies Used
- **Python**
- **Streamlit** – UI framework
- **Pickle** – Model/data loading
- **TMDB API** – For fetching movie posters
- **Pandas & Scikit-learn** (used in backend for data preprocessing & similarity)

## 📁 Project Structure

Movie-Recommender/
├── app.py # Streamlit app
├── model/
│ ├── movie_list.pkl # Movie dataframe
│ └── similarity.pkl # Similarity matrix
├── notebook86c26b4f17.ipynb # Jupyter notebook used for model development
└── README.md # Project documentation

## 🧪 Features
- Recommends movies based on textual similarity of genres, keywords, cast, etc.
- Integrates real-time movie posters from TMDB API.
- User-friendly dropdown interface.

## ▶️ How to Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/ramprasadmundel8/Mini-Projet.git
   cd Movie-Recommender
Install requirements
pip install streamlit requests
Run the Streamlit app
streamlit run app.py

TMDB API Key
Make sure to keep a valid TMDB API key in the code:
url = f"https://api.themoviedb.org/3/movie/{movie_id}?api_key=YOUR_API_KEY&language=en-US"
Replace "YOUR_API_KEY" with your actual TMDB key or store it securely using environment variables or a config file.

🖼️ Sample Output
🎥 Movie Selected	🎯 Recommendations
Inception	Interstellar, The Prestige, Shutter Island, etc.
Avengers	Iron Man, Captain America, Thor, etc.
Each result comes with a poster image fetched from TMDB.


