# 🎬 Movie Recommender System

A powerful and intelligent movie recommendation system built with Python and Streamlit. This application uses machine learning algorithms to recommend movies based on multiple factors including genres, keywords, cast, production companies, and movie tags.

## ✨ Features

- **Personalized Recommendations**: Get movie recommendations based on your favorite films
- **Multiple Recommendation Criteria**:
  - Similar tags and keywords
  - Genre-based recommendations
  - Production company recommendations
  - Cast-based recommendations
- **Movie Details**: View comprehensive information about movies including:
  - Budget, revenue, and runtime
  - Release date and rating
  - Genres, cast, and director
  - Available languages and overviews
  - Movie posters and cast photos
- **Browse All Movies**: Paginated view to explore the entire movie database
- **Cast Information**: Toggle to view actor/actress biographies

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Setup

1. **Clone the repository**

```bash
git clone https://github.com/Ankan-B10/Movie-Recommender-System.git
cd Movie-Recommender-System
```

2. **Create a virtual environment** (optional but recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

## 📖 Usage

1. **Run the application**

```bash
streamlit run main.py
```

2. **Open in browser**
   - The app will automatically open at `http://localhost:8501`

3. **Select an option from the menu**
   - **Recommend me a similar movie**: Select a movie and get personalized recommendations
   - **Describe me a movie**: View detailed information about a specific movie
   - **Check all Movies**: Browse through all available movies with pagination

## 📁 Project Structure

```
Movie-Recommender-System/
├── main.py                          # Main Streamlit application
├── requirements.txt                 # Project dependencies
├── README.md                        # Project documentation
├── processing/
│   ├── __init__.py
│   ├── display.py                  # UI display logic and movie details
│   └── preprocess.py               # Data preprocessing and recommendations
├── Files/
│   ├── tmdb_5000_movies.csv        # Movie database
│   ├── tmdb_5000_credits.csv       # Credits information
│   ├── similarity_tags_*.pkl       # Pre-computed similarity matrices
│   ├── new_df_dict.pkl             # Processed dataframe
│   ├── movies_dict.pkl             # Movies data
│   └── movies2_dict.pkl            # Additional movies data
```

## 🛠️ Technologies Used

- **Streamlit**: Interactive web application framework
- **Pandas**: Data manipulation and analysis
- **scikit-learn**: Machine learning (TF-IDF, Cosine Similarity)
- **NLTK**: Natural language processing
- **Requests**: API calls for movie data and images
- **Python**: Core programming language

## 🎯 How It Works

### Recommendation Algorithm

1. **Data Processing**: The system processes movie data including:
   - Genres, keywords, cast, and production companies
   - Movie overviews and tags
2. **Feature Vectorization**: Uses CountVectorizer to convert text data into numerical vectors

3. **Similarity Calculation**: Computes cosine similarity between movies based on:
   - Tags (overview + genres + keywords + cast + crew)
   - Genres
   - Keywords
   - Production companies
   - Cast

4. **Ranking**: Returns top 5 unique recommendations from the most similar movies

## 📊 Dataset

The project uses the TMDB (The Movie Database) dataset with 5000 movies including:

- Movie metadata (budget, revenue, runtime, rating)
- Cast and crew information
- Production details
- Movie genres and keywords

## 🔧 API Integration

The system integrates with The Movie Database (TMDB) API to fetch:

- Movie posters
- Cast profile images
- Actor biographies

## 📝 Requirements

See `requirements.txt` for complete list of dependencies including:

- streamlit==1.27.2
- pandas==2.1.1
- scikit-learn==1.3.1
- nltk==3.8.1
- And many more...

## 🐛 Troubleshooting

**Issue**: Module not found errors

- **Solution**: Ensure all dependencies are installed: `pip install -r requirements.txt`

**Issue**: API rate limiting

- **Solution**: The app has built-in caching. Clear cache if needed: `streamlit cache clear`

**Issue**: Slow initial load

- **Solution**: The app pre-processes data on first run. Subsequent runs are faster.

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📧 Contact

**Author**: Ankan Bera  
**Email**: beraankan8@gmail.com

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- TMDB (The Movie Database) for the movie dataset and API
- Streamlit community for the amazing framework
- scikit-learn for ML algorithms

---

**Happy Watching! 🍿**
