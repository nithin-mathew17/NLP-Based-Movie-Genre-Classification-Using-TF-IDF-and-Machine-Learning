# NLP-Based-Movie-Genre-Classification-Using-TF-IDF-and-Machine-Learning

## Project Overview

This project is an **Natural Language Processing (NLP)** based machine-learning system that automatically predicts the genre of a movie from its textual description.

The project uses **TF-IDF (Term Frequency-Inverse Document Frequency)** to convert movie descriptions into numerical features and applies two machine-learning algorithms:

* Logistic Regression
* Multinomial Naive Bayes

The performance of both models is evaluated and compared using standard classification metrics.

## Objectives

The main objectives of this project are:

* To develop an NLP-based movie genre classification system.
* To preprocess movie description text.
* To convert text into numerical features using TF-IDF.
* To train machine-learning models for genre classification.
* To compare Logistic Regression and Multinomial Naive Bayes.
* To evaluate model performance using accuracy, precision, recall, F1-score, and confusion matrix.
* To predict the genre of new movie descriptions.


##  Dataset

The project uses a movie genre dataset containing movie information such as:

| Column        | Description                      |
| ------------- | -------------------------------- |
| `TITLE`       | Title of the movie               |
| `GENRE`       | Genre/category of the movie      |
| `DESCRIPTION` | Textual description of the movie |
| `DATE`        | Date/year-related information    |

The original dataset contains multiple movie genres. For this project, the following **8 genres** were selected:

1. Drama
2. Documentary
3. Comedy
4. Short
5. Horror
6. Thriller
7. Action
8. Western

### Dataset Used

**File:** `Movies_Genre_Description.csv`

After filtering the selected genres, the final dataset contained:

* **Training samples:** 72,396
* **Testing samples:** 18,100
* **Total samples:** 90,496

---

## Project Workflow

```text
Movie Description
       ↓
Text Preprocessing
       ↓
TF-IDF Feature Extraction
       ↓
Machine Learning Models
       ↓
Genre Prediction
       ↓
Model Evaluation
```

---

## Text Preprocessing

The movie descriptions are cleaned before applying machine learning.

The preprocessing includes:

* Converting text to lowercase
* Removing punctuation
* Removing unnecessary characters
* Removing extra spaces

### Example

**Before preprocessing:**

```text
I WANT to WATCH this AMAZING movie!!!
```

**After preprocessing:**

```text
i want to watch this amazing movie
```

---

## TF-IDF Feature Extraction

TF-IDF is used to convert the cleaned movie descriptions into numerical feature vectors.

The TF-IDF vectorizer was configured with a maximum of **10,000 features**.

This numerical representation is then provided as input to the machine-learning models.

---

## Machine Learning Models

### 1. Logistic Regression

Logistic Regression was used for multi-class movie genre classification.

It performed better than the Naive Bayes model and was selected as the final model.

### 2. Multinomial Naive Bayes

Multinomial Naive Bayes was implemented as a baseline text-classification model.

It is commonly used for classification problems involving text-based features.

---

## Results

The models were evaluated using the test dataset.

| Model                   | Test Accuracy |
| ----------------------- | ------------: |
| Logistic Regression     |    **69.84%** |
| Multinomial Naive Bayes |    **63.55%** |

### Best Model

**Logistic Regression** achieved the highest test accuracy of:

> **69.84%**

It performed approximately **6.29 percentage points better** than Multinomial Naive Bayes.

---

## Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

The confusion matrix was used to analyze which genres were correctly classified and which genres were confused with one another.

---

## Sample Prediction

The trained model can be used to classify new movie descriptions.

Example:

```text
Input:
A terrifying story about a group of people who encounter a mysterious creature.

Predicted Genre:
Horror
```

The system processes the new description using the same preprocessing and TF-IDF transformation used during training before generating the prediction.

---

## Technologies Used

| Technology / Library       | Purpose                          |
| -------------------------- | -------------------------------- |
| Python                     | Programming language             |
| Pandas                     | Dataset handling                 |
| NumPy                      | Numerical operations             |
| Scikit-learn               | TF-IDF, ML models and evaluation |
| Matplotlib                 | Visualization                    |
| Seaborn                    | Confusion matrix visualization   |
| Regular Expressions (`re`) | Text preprocessing               |
| Google Colab               | Development environment          |

---

## Project Structure

```text
NLP-Movie-Genre-Classification/
│
├── Movies_Genre_Description.csv
│
├── NLP_Movie_Genre_Classification.ipynb
│
├── README.md
│
├── screenshots/
│   ├── 01_dataset_preview.png
│   ├── 02_genre_distribution.png
│   ├── 03_text_preprocessing.png
│   ├── 04_tfidf_output.png
│   ├── 05_logistic_regression_report.png
│   ├── 06_naive_bayes_report.png
│   ├── 07_model_comparison.png
│   ├── 08_confusion_matrix.png
│   └── 09_sample_predictions.png
│
└── report/
    └── NLP_Project_Report.pdf
```

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Open the Jupyter Notebook

Open:

```text
NLP_Movie_Genre_Classification.ipynb
```

The notebook can be run using:

* Google Colab
* Jupyter Notebook
* JupyterLab

### 3. Upload the dataset

Make sure the following file is available:

```text
Movies_Genre_Description.csv
```

### 4. Run the notebook

Execute the notebook cells sequentially.

The notebook will:

1. Load the dataset
2. Explore the data
3. Select the required genres
4. Preprocess the descriptions
5. Generate TF-IDF features
6. Train Logistic Regression
7. Train Multinomial Naive Bayes
8. Evaluate both models
9. Generate the confusion matrix
10. Predict genres for new movie descriptions

---

## Limitations

The project has some limitations:

* Only 8 genres were selected from the available dataset.
* The Logistic Regression model achieved 69.84% accuracy, so some descriptions are still misclassified.
* TF-IDF does not deeply understand the semantic context of a sentence.
* Some movie genres contain similar vocabulary and themes.
* The system does not use advanced contextual language models.

---

## Future Scope

The project can be improved by:

* Including more movie genres.
* Using a larger and more diverse dataset.
* Improving text preprocessing.
* Experimenting with Support Vector Machines and other classifiers.
* Using word embeddings.
* Exploring transformer models such as BERT.
* Developing a web-based movie genre prediction interface.
* Supporting multi-label genre classification.
* Improving classification between similar genres.

---

## Project Screenshots

Screenshots of the dataset, preprocessing, model evaluation, confusion matrix, and prediction results are available in the `screenshots/` folder.

---

## Project Report

The complete project report is available in:

```text
report/NLP_Project_Report.pdf
```

---

## Author

**Name:** NITHIN MATHEW
**Register Number:** 24UBC148
**Class:** III BCA A
**Course:** Natural Language Processing

---

## Conclusion

This project demonstrates how traditional NLP techniques can be combined with machine learning to automatically classify movie genres from textual descriptions.

TF-IDF was used for feature extraction, while Logistic Regression and Multinomial Naive Bayes were used for classification. Logistic Regression achieved the best performance with a test accuracy of **69.84%**.

The project provides a practical example of an end-to-end NLP classification pipeline, from text preprocessing and feature extraction to model training, evaluation, and prediction.
