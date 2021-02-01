

# PIA: Pain in Antiquity - Distant Reading of **Corpus Hippocraticum**

---

## Purpose
This repo contains scripts used in an article anlyzing theory of pain in **Corpus Hippocraticum**. The scripts have a form of Jupyter notebooks and serve to analyze texts within the corpus by means of computational methods from the areas of natural language processing and corpus linguistics, especially by means of distributional semantic models.

---
## Authors
* Vojtěch Kaše [![](https://orcid.org/sites/default/files/images/orcid_16x16.png)]([0000-0002-6601-1605](https://www.google.com/url?q=http://orcid.org/0000-0002-6601-1605&sa=D&ust=1588773325679000)), SDAM project, vojtech.kase@gmail.com
* Vojtěch Linka,  Charles University, vojtech.p.linka@gmail.com

## License
CC-BY-SA 4.0, see attached License.md

## DOI
[Here will be DOI or some other identifier once we have it]

### References
[Here will go related articles or other sources we will publish/create]

---
# How to use this repository

## Sources and prerequisites

### Data
The scripts in this repo rely on LAGT dataset, accessible via sciecedata.dk. 


### Software
The scripts are for Python 3 programming language and require especially the following Python libraries:
1. sddk (for data exchange with sciencedata.dk)
2. pandas (data are formatted as pandas dataframes)
3. numpy (matrix operations)
4. scikit-learn (word embeddings)
5. matplotlib (plotting)


### Registered account
1. sciencedata.dk (not necessary, but useful)
1. google (not necessary, but useful)


---
## Instructions 
The scripts are in the `scripts` subfolder and their numbers and titles should be self-explanatory:
* [1_EXTRACTING-CORPORA.ipynb](1_EXTRACTING-CORPORA.ipynb) extracts relevant texts from a large corpus of ancient Greek texts (LAGT).
* [2_EXPLORATIONS+REPLACEMENT.ipynb](scripts/2_EXPLORATIONS+REPLACEMENT.ipynb) makes some preliminary observations and employs regular expression to extract all pain words unified under four word roots: πόνο*, ὀδύν*, ἄλγ*, λύπ*.
* [3_OVERVIEW+WORK-DISTANCES.ipynb](scripts/3_OVERVIEW+WORK-DISTANCES.ipynb) (1) offers a detailed overview of frequecies of the pain  words across individual works and work categories; (2) generates plots visualizing distances between works based on their shared vocabulary.
* [4_PAIN-SENTENCES.ipynb](scripts/4_PAIN-SENTENCES.ipynb) analyzes sentences comparing the pain words, comparing them agaist the rest of the corpus.
* [5_VECTORS.ipynb](scripts/5_VECTORS.ipynb) introduces a vector (or: distributional) semantic model. It construts a weighted word-word co-occurrence matrix using the PPMI3 metric, transforms it by SVD and compares row vectors corresponding to individual words by means of cosine similarity. Finally, it plots the embeddings projected into a 2-dimensional space by tSNE.
