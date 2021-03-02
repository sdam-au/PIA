

# PIA: Pain in Antiquity (under review)

---

## Purpose
This repository serves as a supplementary material for the article "Is There a Theory of Pain in Corpus Hippocraticum? A Distributional Semantic Analysis", currently under review (March 2021). It contains scripts, data and figures. The scripts are in Python 3 programming language and have a form of Jupyter notebooks. All our analyses aim at being fully reproducible and we invite other scholars to reuse our code and data for their analyses.   

---
## Authors
* anonymized (article currently under review)

## License
CC-BY-SA 4.0, see attached License.md

---
# How to use this repository

* download or clone the repository
* activate the virtual environment (open your command line, move the the repository folder and run `bash ./create_pia_venv.sh`)
* in the jupyter notebooks, always check that you are connected to the *pia_venv* kernel
* (alternatively, if you do not wish to use the virtual environment, make sure that you have installed all required python packages within the `requirements.txt` file: `pip install -r requiremnts.txt`

---
## Jupyter notebooks 
The scripts are in the `scripts` subfolder and their numbers and titles should be self-explanatory:
* [1_EXTRACTING-CORPORA.ipynb](1_EXTRACTING-CORPORA.ipynb) extracts relevant texts from a large corpus of ancient Greek texts (LAGT).
* [2_EXPLORATIONS+REPLACEMENTS.ipynb](scripts/2_EXPLORATIONS+REPLACEMENTS.ipynb) makes some preliminary observations and employs regular expression to extract all pain words unified under four word roots: πόνο*, ὀδύν*, ἄλγ*, λύπ*.
* [3_OVERVIEW+WORK-DISTANCES.ipynb](scripts/3_OVERVIEW+WORK-DISTANCES.ipynb) (1) offers a detailed overview of frequecies of the pain  words across individual works and work categories; (2) generates plots visualizing distances between works based on their shared vocabulary.
* [4_PAIN-SENTENCES.ipynb](scripts/4_PAIN-SENTENCES.ipynb) analyzes sentences comparing the pain words, comparing them agaist the rest of the corpus.
* [5_VECTORS.ipynb](scripts/5_VECTORS.ipynb) introduces a vector (or: distributional) semantic model. It construts a weighted word-word co-occurrence matrix using the PPMI3 metric, transforms it by SVD and compares row vectors corresponding to individual words by means of cosine similarity. Finally, it plots the embeddings projected into a 2-dimensional space by tSNE.
* [5_VECTORS_without-de-diaeta.ipynb](scripts/5_VECTORS_without-de-diaeta.ipynb) is the same script as the previous one, with one difference: the work *De diaeta*
is excluded from the analysis.
