📌 Project Overview

This project predicts the genre of a movie based on its plot summary using Natural Language Processing (NLP) and Machine Learning.
The system analyzes movie descriptions, converts text into numerical features using TF-IDF Vectorization, and classifies them into genres such as Drama, Comedy, Horror, Thriller, Action, Documentary, and more.

This project demonstrates the complete workflow of a text classification problem, including:

dataset loading
text preprocessing
exploratory data analysis (EDA)
model training
model comparison
prediction on unseen data
🎯 Objective

The main objective of this project is to build a machine learning model that can automatically predict movie genres from textual plot descriptions.

This can be useful for:

movie recommendation systems
content categorization
streaming platforms
automated tagging systems
🚀 Features
Automatically downloads dataset using KaggleHub
Loads and parses IMDb movie genre dataset
Performs Exploratory Data Analysis (EDA)
Cleans and preprocesses movie plot summaries
Converts text into numerical form using TF-IDF
Trains and compares 3 machine learning models
Selects the best-performing model
Generates visualizations
Predicts movie genres for:
validation data
test dataset
custom user input plots
🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
KaggleHub
Natural Language Processing (NLP)
🤖 Machine Learning Models Used

This project trains and compares the following models:

Multinomial Naive Bayes
Logistic Regression
Linear Support Vector Machine (Linear SVM)

The best model is selected based on:

Accuracy
Weighted F1 Score
📂 Dataset

This project uses the IMDb Genre Classification Dataset from Kaggle.

Dataset contains:
Movie ID
Movie Title
Genre
Plot Summary

The dataset is automatically downloaded in the code using:

path = kagglehub.dataset_download("hijest/genre-classification-dataset-imdb")
⚙️ Project Workflow
1. Dataset Download

The dataset is downloaded automatically using KaggleHub.

2. Data Loading

The training and test files are loaded and converted into Pandas DataFrames.

3. Exploratory Data Analysis (EDA)

The project performs:

dataset preview
genre distribution analysis
missing value check
4. Text Preprocessing

Movie plot summaries are cleaned by:

converting text to lowercase
removing special characters
removing extra spaces
5. Feature Extraction

Text data is converted into numerical features using:

TF-IDF Vectorizer
Unigrams + Bigrams
50,000 maximum features
6. Model Training

Three machine learning models are trained on the cleaned movie plots.

7. Model Evaluation

Each model is evaluated using:

Accuracy
Weighted F1 Score
Classification Report
8. Best Model Selection

The model with the best performance is automatically selected.

9. Test Prediction

The best model is used to predict genres for the unseen test dataset.

10. Demo Predictions

The project also predicts genres for manually written sample movie plots.

📊 Evaluation Metrics

The following metrics are used to evaluate model performance:

Accuracy Score
Weighted F1 Score
Classification Report

These metrics help compare how well each model performs on different movie genres.

📈 Output Files Generated

The project automatically creates the following output files:

1. genre_distribution.png

Shows the top 15 movie genres in the training dataset.

2. model_comparison.png

Compares model performance based on:

Accuracy
Weighted F1 Score
3. test_predictions.csv

Contains predicted genres for the test dataset.

🧪 Example Demo Predictions

The project includes sample predictions such as:

Action
Romance
Horror
Comedy

Example:

Input  : A retired soldier must fight off a group of dangerous mercenaries...
Predicted Genre: action
▶️ How to Run the Project
1️⃣ Clone the Repository
git clone https://github.com/your-username/movie-genre-prediction.git
cd movie-genre-prediction
2️⃣ Install Required Packages
pip install kagglehub pandas numpy matplotlib seaborn scikit-learn
3️⃣ Run the Python File
python "movie genre prediction.py"
📁 Project Structure
movie-genre-prediction/
│
├── movie genre prediction.py
├── README.md
├── requirements.txt
├── genre_distribution.png
├── model_comparison.png
└── test_predictions.csv
💡 Sample Code Highlights
Text Cleaning Function
def clean_text(text: str) -> str:
    text = text.lower()
    text = re.sub(r"[^a-z\s]", " ", text)
    text = re.sub(r"\s+", " ", text).strip()
    return text
TF-IDF Feature Extraction
tfidf_params = dict(
    max_features=50_000,
    ngram_range=(1, 2),
    sublinear_tf=True,
    min_df=2,
    strip_accents="unicode",
    analyzer="word",
    token_pattern=r"\b[a-z]{2,}\b",
)
Models Used
- MultinomialNB
- LogisticRegression
- LinearSVC
🔥 Key Learnings from This Project

Through this project, I learned:

how to handle text datasets
how to preprocess natural language data
how TF-IDF vectorization works
how to train and compare machine learning classification models
how to evaluate NLP models using proper metrics
how to build a complete end-to-end ML pipeline
📌 Future Improvements

This project can be improved further by:

adding stopword removal
using stemming / lemmatization
applying hyperparameter tuning
trying deep learning models such as:
LSTM
GRU
BERT
Transformers
building a web app using:
Flask
Streamlit
📍 Conclusion

This project successfully demonstrates how Natural Language Processing and Machine Learning can be used to solve a real-world movie genre classification problem.

By analyzing movie plot summaries, the model can automatically predict genres and help in organizing and recommending movie content more efficiently.

👩‍💻 Author

Your Name
B.Tech CSE (AI & ML) Student
Interested in Machine Learning, NLP, Computer Vision, and AI Projects

⭐ If You Like This Project

If you found this project useful, consider:

⭐ starring the repository
🍴 forking it
🛠️ improving it further
✅ Also create this requirements.txt

Put this in a file named requirements.txt:

kagglehub
pandas
numpy
matplotlib
seaborn
scikit-learn
✅ Small suggestion

Your README is already good now, but to make GitHub look more professional, you should also add:

requirements.txt
.gitignore
output screenshots
your best model accuracy in README


