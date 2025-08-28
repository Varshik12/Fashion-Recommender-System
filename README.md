# fashion-recommender-system
A deep learning-based application for recommending visually similar fashion items using image embeddings.

Overview
This project implements a Content-Based Fashion Recommender System, leveraging the ResNet50 neural network to extract image features and the Nearest Neighbors algorithm to recommend top visually similar products. The system is built with Python, TensorFlow, and Streamlit for interactive web-based recommendations.

Features
Extracts image embeddings using a pre-trained ResNet50 model.

Processes uploaded fashion item images and recommends similar items based on visual features.

Interactive Streamlit UI for uploading images and viewing recommendations.

Efficient similarity search using sklearn's NearestNeighbors with Euclidean distance.

Fast and scalable embedding management using pickle serialization.

How It Works
Image Feature Extraction:
Each image in the product database is processed to extract normalized feature embeddings using ResNet50.

Similarity Search:
When a user uploads a fashion image, its embedding is compared against stored embeddings using Nearest Neighbors to find the closest matches.

Recommendation Display:
The top 5 visually similar items are displayed on the web interface, allowing users to explore similar fashion options.

Installation
Clone this repository.

Install required Python packages:

text
pip install tensorflow streamlit scikit-learn pillow tqdm
Place product images inside the images directory.

Run app.py to generate embeddings:

text
python app.py
Launch the Streamlit app:

text
streamlit run main.py
Usage
Upload any fashion item image via the Streamlit interface.

Instantly view top visually similar product recommendations.

Files
app.py: Generates image embeddings for all fashion items in the database.

main.py: Runs the Streamlit web UI and recommendation engine.

test.py: Script for testing recommendations via command line.

embeddings.pkl, filenames.pkl: Pickled data files containing product embeddings and file paths.

Acknowledgements
ResNet50 model from TensorFlow Keras Applications.

scikit-learn for efficient similarity search.


