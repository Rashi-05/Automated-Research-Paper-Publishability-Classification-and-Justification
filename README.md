# Automated-Research-Paper-Publishability-Classification-and-Justification
## Project Overview :-
This project aims to **automate the process of classifying research papers as Publishable or Non-Publishable** using semantic embeddings and machine learning.
## Objective :-
Develop a pipeline to automatically predict publishability of papers.
Provide clear and interpretable justifications for each decision.
## Datastet Overview :-
The dataset used consists of research papers in PDF format. Each paper contains the full text of the submission.The dataset has total 150 ppapers out of which 15 are labeled papers(used for training) as publishable and not publishable and remaining 135 are to labeled.
## Tools and Packages
Python (v3.x),PyMuPDF (fitz) for PDF text extraction,SentenceTransformers for semantic embeddings,scikit-learn for Logistic Regression,re (Python’s standard library) for text processing,Pandas for data handling.
## Methadology :-
1) Importing various required libraries numpy,pandas,PyPDF2,sentence_transformers
2) PDF text extraction :- To extract and clean text from PDF papers
3) Dataset Structuring :- Sructured the dataset into labeled (Publishable or Non-Publishable) and unlabeled sets. For labeled documents, included the label (1 for Publishable, 0 for Non-Publishable).
4) Text Cleaning :- Cleaned and standardized dataset by removed references, non-ASCII symbols, brackets,excess whitespace and number annotations,converted text to lowercase.Also filtered out documents with fewer than 100 words to keep only those suitable for training or evaluation.
5) Section Extraction:- Extracted semantic sections (Introduction, Methodology, etc.)
6) Handling missing values :- Handled missing values in various section.
7) Semantic Embedding: Transformed documents into vector embeddings with sentence transformers.
8) Classification: Logistic regression(selected as fianl model) to predict publishability.
9) Threshold Tuning: Adjust decision threshold to account for class imbalance.
10) (LLM based)Justification Generation: Provide clear explanations for each decision.
## Results :-
We evaluated multiple models using 5-fold cross-validation. Logistic Regression also performed well with an F2 score of 0.93.As it is faster and more reliable with small data, making it a convenient choice 
## Conclusion :-
This project successfully demonstrated the process of training, evaluating, and selecting a machine learning classifier. Logistic Regression was ultimately chosen due to its strong performance and faster training time, making it a reliable solution for our application. 

