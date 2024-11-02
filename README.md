# Movie Recommendation System

This project is a **Content-Based Movie Recommendation System** built using Python. It recommends movies based on the similarity between movies, using metadata like movie descriptions, genres, and keywords. The system is deployed on **Heroku** for easy access.

## Features

- **Content-Based Filtering**: Recommends movies based on a provided movie's metadata.
- **Cosine Similarity**: Measures similarity between movies based on their descriptions and other metadata.
- **TF-IDF Vectorization**: Transforms text data (movie plot, genres) into meaningful numeric vectors for comparison.
- **Flask Web Application**: Provides a simple interface for users to input a movie and get recommendations.
- **Deployed on Heroku**: Publicly accessible and easy to use.

## Dataset

The dataset used in this project is from [The Movie Dataset (TMDb)](https://www.themoviedb.org/). You can download the dataset used for this recommender system from the following link:

[Download the movie dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

- **Size**: ~26,000 movies
- **Columns**: `id`, `title`, `overview`, `genres`, `keywords`, `cast`, `crew`

## Requirements

- Python 3.7+
- Flask
- Pandas
- Scikit-learn
- Gunicorn (for Heroku deployment)
- Heroku CLI (for deployment)

## Installation

To run the project locally, follow these steps:

1. **Clone the repository**:

    ```bash
    git clone https://github.com/yourusername/movie-recommendation-system.git
    cd movie-recommendation-system
    ```

2. **Set up a virtual environment (optional but recommended)**:

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # For macOS/Linux
    # or
    venv\Scripts\activate     # For Windows
    ```

3. **Install dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

4. **Run the Flask application**:

    ```bash
    python app.py
    ```

5. **Access the app**:

    Open a browser and visit `http://127.0.0.1:5000`.

## Project Structure

```plaintext
├── app.py                  # Main Flask application
├── models.py               # Recommendation logic
├── movie_dataset.csv        # Dataset containing movie metadata
├── requirements.txt        # Python dependencies
├── Procfile                # Heroku deployment configuration
├── static/                 # Static files like CSS and images
├── templates/              # HTML templates for Flask
└── README.md               # Project documentation
