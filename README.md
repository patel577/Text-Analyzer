# Text-Analyzer
Analyzing text file from corpus and estimate co-similarity between two files by calculating TF-IDF values from scratch. 

# Data
The corpus data is stored under masc_500k_text folder. There are two types of text transcript stored under the folder. 1) Spoken and 2) Written
Each of folder has tanscript of various categories such as emails, jokes, letters, news papers etc. 

# Approach
The main goal of the project is to calcuate TFIDF score for each document and cosimilarity between two documents or categories using pyspark functions. I used 
argparse to make code that can be easily re-use for any text file under the corpus through command-line interface. It helps to change arguments in CLI.

python TextAnalyzer.py function input output --other arguments(optional) 

For example, if you want to compute only TF of all words apppering in document (hotel-california.txt) then,
by running,

python TextAnalyzer.py TF \ ./masc_500k_texts/written.fiction/hotel-california.txt .\hotel-california.tf

which creates a directory called hotel-california.tx and it contains the results of term frequency values.

# Results
We can compute the cosine similarities between any two categories from corpus. I stored the cosimilarity matrix of face-to-face, fiction and spam
into result folder. 


**note: I didn't use any library to calculate TF-IDF score. I make my own function to calcuate the score from scratch. 
