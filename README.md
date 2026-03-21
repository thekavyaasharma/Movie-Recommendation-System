# Movie Recommendation System using NLP 

A movie recommendation web app that suggests up to **9 similar movies** based on a combination of features like overview, keywords, genres, cast, and crew. Built using Python, NLP techniques, and deployed with Streamlit.

---

##  Project Overview

Many viewers want suggestions for movies similar to one they like. This project generates movie recommendations by combining multiple metadata features (overview, keywords, genres, cast, crew), vectorizing the text, applying stemming, and computing similarity scores. The result is an easy-to-use interface to find related films.

---

##  Features

- Combines multiple metadata features (overview, genres, cast, crew, keywords)  
- Uses vectorization (TF-IDF / Count Vectorizer) + text preprocessing (stemming)  
- Computes similarity matrix to find top 9 movie recommendations  
- Streamlit-based frontend for user interaction  
- Deployed on Streamlit Community Cloud — accessible via web  
- Includes both the code (Jupyter notebook + `app.py`) and serialized models/data files (`.pkl`)

---

##  File Structure

| File | Description |
|---|---|
| `Movie-recommendation-system.ipynb` | Notebook with exploratory data analysis, preprocessing, feature engineering & model building |
| `app.py` | Streamlit application script for frontend + backend interaction |
| `tmdb_5000_movies.csv` | Raw TMDB dataset used for building the system |
| `movies_dict.pkl` | Pickled dictionary of movie metadata (for fast lookup) |
| `similarity.pkl` | Precomputed similarity matrix between movies |
| `requirements.txt` | List of Python dependencies |

---

## 🛠️ Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/thekavyaasharma/Movie-Recommendation-System.git
   cd Movie-Recommendation-System
  

2. **Create a virtual environment (optional but recommended)**
    ```bash
    python3 -m venv venv
    source venv/bin/activate       # on macOS/Linux
    venv\Scripts\activate          # on Windows

3. **Install required packages**
   ```bash
   pip install -r requirements.txt

4. **Run Locally**
   ```bash
   streamlit run app.py

5. **Open in browser**
   The app should open at http://localhost:8501 (or the URL shown by Streamlit).
---

## Live Demo & Code Repo

 - Live Demo: movie-recommendation-system-ks18.streamlit.app
 - Source Code: https://github.com/thekavyaasharma/Movie-Recommendation-System
---

## 🤖 How It Works (High Level)

###  Data Loading & Cleaning
- Load TMDB dataset  
- Handle missing values  
- Extract relevant columns (**overview**, **genres**, **cast**, **crew**, **keywords**)

### ⚙️ Feature Engineering
- Tokenize, remove stopwords, and apply stemming/lemmatization  
- Combine metadata features into a single **“soup”** string for each movie

### 🧮 Vectorization & Similarity
- Apply **TF-IDF** (or **Count Vectorizer**) on the combined text  
- Compute pairwise similarity matrix (e.g., **cosine similarity**)

### 🎯 Recommendation Logic
- For a selected movie, fetch its similarity scores  
- Recommend top **9 similar movies**, excluding the selected one

### 💻 Frontend Integration
- Use **Streamlit** to allow users to select a movie  
- Display recommendations with **poster images** (if extended)
---

## 📂 Extend & Improve (Ideas)

- Include poster images using **TMDB API**  
- Add genre weighting or custom feature weights  
- Try advanced embeddings (**Word2Vec**, **Doc2Vec**, **BERT**)  
- Improve performance using **Approximate Nearest Neighbors**  
- Add user ratings or feedback-based personalization  
- Deploy via **Docker** or cloud (**Heroku, AWS**, etc.)
---

## ✅ Requirements

Make sure you have:

- **Python 3.7+**  
- All dependencies listed in `requirements.txt`  
- **Internet connection** (if extending with TMDB API/posters)

---

## 👏 Acknowledgements & References

- 🎬 **TMDB dataset** (The Movie Database)  
- 📚 Tutorials and blogs on content-based movie recommenders  
- 💡 Streamlit documentation
---

## 👩‍💻 Author

**Kavya Sharma**  
- GitHub: [https://github.com/thekavyaasharma](https://github.com/thekavyaasharma)  
- LinkedIn: [https://www.linkedin.com/in/thekavyaasharma](https://www.linkedin.com/in/thekavyaasharma)  
- Passionate about **Data Science, Machine Learning, and AI projects**

---

##  Thank You

Thank you for checking out my project!  
Feel free to **explore the code**, **try the live demo**, and **share your feedback**.  

Happy Movie Discovering! 

