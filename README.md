# Spam Mail Detector

A text-classification project developed for the **QSkill Artificial Intelligence & Machine Learning Internship**. It uses the SMS Spam Collection dataset to classify messages as **spam** or **ham** (non-spam).

## Internship Details

- **Domain:** Artificial Intelligence & Machine Learning
- **Internship period:** 14 September 2026 – 14 October 2026
- **Selected task:** Spam Mail Detector

## Objective

Build a machine learning classifier that distinguishes spam messages from legitimate messages using text preprocessing, TF-IDF feature extraction, and Naive Bayes classifiers.

## Dataset

The notebook downloads the SMS Spam Collection dataset through `kagglehub`:

- Kaggle dataset identifier: `uciml/sms-spam-collection-dataset`
- Expected CSV file: `spam.csv`
- Original message and label columns: `v2` and `v1`
- The notebook removes unused columns, renames the relevant columns, checks for missing values and duplicate rows, and removes duplicate messages.

The notebook's saved outputs show 5,572 rows before duplicate removal and 5,169 rows afterward.

## Project Workflow

1. Download and load the dataset.
2. Inspect the data and remove irrelevant columns.
3. Rename the label and message columns and encode the labels.
4. Check missing values and remove duplicate rows.
5. Explore the class distribution and message length using charts and descriptive statistics.
6. Preprocess text by lowercasing, tokenizing, removing stopwords and punctuation, and stemming words.
7. Visualize frequent words using word clouds.
8. Convert processed messages into numeric features using TF-IDF.
9. Split the data into training and test sets.
10. Train and compare Gaussian Naive Bayes, Multinomial Naive Bayes, and Bernoulli Naive Bayes.
11. Evaluate models using accuracy and precision.

## Libraries and Tools

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- WordCloud
- scikit-learn
- kagglehub

## Repository Contents

- `Spam Mail Detection.ipynb` — notebook containing dataset loading, exploration, preprocessing, visualizations, TF-IDF feature extraction, model training, and evaluation.
- `README.md` — project overview and instructions.
- `requirements.txt` — Python dependencies.

## Setup and Usage

### 1. Clone or download the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

Replace the placeholders with your actual GitHub repository URL and folder name.

### 2. Create and activate a virtual environment (recommended)

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\\Scripts\\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook &
```

Open `Spam Mail Detection.ipynb` and run the cells from top to bottom. The notebook downloads the dataset using `kagglehub`, so an internet connection may be required. If Kaggle access or authentication is requested in your environment, follow Kaggle's current setup instructions.

NLTK resources such as tokenizers and English stopwords are downloaded by the notebook when needed.

## Results in the Saved Notebook

The notebook contains two model experiments with different TF-IDF settings and train/test splits. In the later experiment, using `max_features=3000` and a 20% test split, the saved results are:

| Model | Accuracy | Precision |
|---|---:|---:|
| Gaussian Naive Bayes | 86.17% | 49.38% |
| Multinomial Naive Bayes | 97.00% | 100.00% |
| Bernoulli Naive Bayes | 97.87% | 99.17% |

These figures are the notebook's **saved outputs**, not a guarantee of the results after a fresh run.

## QSkill Requirement Coverage

| QSkill requirement | Project coverage |
|---|---|
| Load messages and labels | Loads the SMS Spam Collection dataset and uses message text and spam/ham labels |
| Preprocess text | Lowercasing, tokenization, stopword removal, punctuation filtering, and stemming |
| Convert text into numeric features | TF-IDF |
| Split into training and test sets | Uses `train_test_split` |
| Train a simple model | Compares Gaussian, Multinomial, and Bernoulli Naive Bayes |
| Measure performance | Calculates accuracy and precision |

## Author
Completed by Mohammed Shoaib.

Prepared for the QSkill AI & ML Internship.
