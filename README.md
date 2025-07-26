Movie Recommender System

Overview:
This project implements a personalized Movie Recommender System designed to combat decision fatigue in movie selection. By leveraging user preferences and movie metadata, it provides intuitive and enjoyable recommendations, enhancing the overall movie-watching experience.

Features:
Interactive Movie Search: Users can easily search for their favorite movies with real-time suggestions.

Popular Movie Browsing: A paginated display allows users to explore popular movies.

Rich Movie Details: Displays comprehensive information for selected movies, including posters, IMDb ratings, taglines, top actors, directors, and genres, fetched dynamically from the TMDB API.

Personalized Filtering: Recommendations can be refined using filters for preferred actors, directors, genres, and even a user's current mood.

Dynamic Recommendations: Generates a list of tailored movie recommendations based on user input, complete with reasons for each suggestion.

Responsive User Interface: Built with Streamlit, ensuring a clean, intuitive, and adaptive experience across various devices.

Technologies Used:

Python: The core programming language for all logic.

Streamlit: For building the interactive and responsive web user interface.

Pandas: For data manipulation and processing of the local movie dataset.

The Movie Database (TMDB) API: For fetching real-time movie posters, ratings, and taglines.

Methodology:

The project follows a modular and structured approach:

Data Acquisition & Preparation: A local dataset of movie titles and internal identifiers forms the basis.

API Integration: Functions in utils.py handle fetching supplementary movie details from the TMDB API.

Recommendation Logic: The model.py module contains the content-based recommendation algorithm, which suggests movies based on similarity in genres, actors, and directors, incorporating mood as a filter.

Streamlit UI: The app.py file orchestrates the user interface, managing session state, user inputs, and displaying results.

Project Structure


├── app.py              
├── model.py             
├── utils.py             
├── data/                
└── README.md           

How to Run the Project
Clone the repository:

git clone <your-repo-url>
cd movie-recommender-system

Install dependencies:

pip install -r requirements.txt

(Note: You'll need to create a requirements.txt file listing all Python dependencies like streamlit, pandas, requests (if used for API calls), etc.)

Set up TMDB API Key:

Obtain an API key from The Movie Database (TMDB).

You might need to store this key as an environment variable or configure it within utils.py (e.g., TMDB_API_KEY = "your_key_here").

Run the Streamlit application:

streamlit run app.py

The application will open in your web browser.

Further Works
Advanced Recommendation Algorithms: Implement collaborative filtering or hybrid models for more sophisticated recommendations.

User Authentication & Profiles: Allow users to create accounts, save preferences, and track watch history.

Expanded Data Features: Incorporate more detailed metadata (e.g., plot summaries, keywords) for richer recommendations.

Streaming Service Integration: Add links to where movies can be streamed on various platforms.

Performance Optimization: Implement aggressive caching and explore database integration for scalability.
