# Automated-Research-Paper-Publishability-Classification-and-Justification
## Project Overview :-
This project aims to **automate the process of classifying research papers as Publishable or Non-Publishable** using semantic embeddings and machine learning.
## Objective :-
-Develop a pipeline to automatically predict publishability of papers.
-Provide clear and interpretable justifications for each decision.
## Datastet Overview :-
The dataset consists of **research papers in PDF format**. Each paper contains the full text of the submission.The dataset includes:
- **15 labeled papers** (with publishability label).
- **135 unlabeled papers** (without label).
## Tools and Packages
-**Python (v3.x)**
- **PyMuPDF (fitz)** for PDF text extraction
- **SentenceTransformers** for semantic embeddings
- **scikit-learn** for Logistic Regression
- **re** (Python’s standard library) for text processing
- **Pandas** for data handling
## Methadology :-
1) Importing libraries (numpy,pandas,PyPDF2,sentence_transformers).
2) PDF text extraction :- Extract and clean text from PDF papers.
3) Dataset structuring :- Split into labeled (Publishable or Non-Publishable) and unlabeled sets.
4) Text Cleaning :- Remove references, non-ASCII symbols, brackets,excess whitespace,number annotations; converted text to lowercase. Filter out documents with < 100 words.
5) Section Extraction:- Extract semantic sections (Introduction, Methodology, etc.).
6) Handling missing values in various sections.
7) Semantic Embedding: Transformed documents into vector embeddings with sentence transformers.
8) Classification: Logistic regression(selected as final model) to predict publishability.
10) (LLM based) Justification Generation: Provide clear explanations for each decision.
## Results :-
We evaluated multiple models using 5-fold cross-validation. Logistic Regression performed well with an F2 score of 0.93. It was faster and more reliable with small data, making it a convenient choice. 
## Conclusion :-
This project successfully demonstrated the process of training, evaluating, and selecting a machine learning classifier. Logistic Regression was ultimately chosen due to its strong performance and faster training time, making it a reliable solution for our application. 
## How to Use 

1. **Clone the repository:**

```bash
git clone https://github.com/your-username/Automated-Research-Paper-Publishability-Classification-and-Justification.git
cd Automated-Research-Paper-Publishability-Classification-and-Justification

```

2. **Installing requirements:**

```bash
pip install -r requirements.txt
```
This installs all the necessary libraries for the project.

3. **Open the notebook in Google Colab:**
-> Upload the notebook to Google Colab:
-Go to https://colab.research.google.com/
-File -> Upload notebook
-Select cleaned notebook.

4. **Running the pipeline:**
-The notebook guides you through:
-Extracting text from PDF files
-Cleaning and preparing the data
-Generating semantic embeddings with sentence transformers
-Training Logistic Regression for publishability prediction
-Providing publishability predictions alongside justifications for each paper

