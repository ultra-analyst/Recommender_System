### Project: Music Recommendation System

#### Overview
This project demonstrates the creation of a music recommendation system using a dataset of Spotify tracks from the 2000s. The system employs content-based filtering to recommend songs based on features such as beats per minute, energy, danceability, loudness, and more. The recommendation engine is built using Python, Flask, and various machine learning techniques, and is deployed via a web interface that resembles Spotify.

#### Features
- **Data Preprocessing**: Normalization of numerical features and encoding of categorical features.
- **Content-Based Filtering**: Uses cosine similarity and euclidean distances to find and recommend similar songs.
- **Web Interface**: A simple and clean UI built with Flask and styled to resemble Spotify.
- **Deployment**: Hosted using Ngrok to expose the Flask application for easy access.

#### Dataset
The dataset used is the "Spotify-2000" dataset from Kaggle, containing detailed information about 2000 songs, including attributes like tempo, energy, danceability, and more.

#### Implementation Steps
1. **Data Preprocessing**:
   - Normalized numerical features: Beats Per Minute (BPM), Energy, Danceability, Loudness (dB), etc.
   - Encoded categorical features: Artist, Top Genre, Year.

2. **Model Building**:
   - Created a content feature matrix combining normalized numerical and encoded categorical features.
   - Computed similarity matrices using cosine similarity and euclidean distances.
   - Combined similarity matrices for improved recommendations.

3. **Web Application**:
   - Developed a Flask web application to serve the recommendation system.
   - Created HTML templates for the home and recommendations pages.
   - Styled the web pages with CSS to resemble Spotify's interface.

4. **Deployment**:
   - Used Ngrok to expose the local Flask application to the internet.
   - Set up Ngrok authtoken for authenticated usage.

#### Usage
1. **Data Preprocessing and Model Building**:
   - Run the notebook `model_building.ipynb` to preprocess the data and build the model.
   - Ensure the output files `combined_similarity_matrix.npy` and `processed_dataset.csv` are saved.

2. **Running the Flask App**:
   - Run the notebook `app_notebook.ipynb` to start the Flask application.
   - Use Ngrok to obtain a public URL and access the web interface.

#### How to Run Locally
1. Clone the repository:
   ```sh
   git clone https://github.com/ultra-analyst/Recommender_System.git
   cd Recommendation_System
   ```

2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

3. Preprocess data and build the model:
   - Run `Recommender_Model.ipynb` in Jupyter Notebook or Jupyter Lab.

4. Start the Flask app:
   ```sh
   python app.py
   ```

5. Expose the Flask app using Ngrok:
   ```sh
   ngrok http 5000
   ```

6. Access the web interface using the Ngrok public URL (Enter your ngrok Authtoken).

#### Technologies Used
- **Python**: For data preprocessing, model building, and backend development.
- **Flask**: For creating the web application.
- **Ngrok**: For exposing the local Flask app to the internet.
- **Pandas and NumPy**: For data manipulation and numerical operations.
- **Scikit-learn**: For normalization, encoding, and similarity calculations.
