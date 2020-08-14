# Author Classification with BERT

## Abstract
Authorship classification is an essential topic in Natural Language Processing, and it can be used in tasks such as identifying most likely authors of documents, plagia- rism checking, and as a new way for rec- ommending authors to readers based on the reader’s preferred style of writing. In this project, we explored this problem at different levels, with different deep learning models and with different implementations of com- bining BERT embeddings with bag of words in a neural network on the Reuters_50_50 dataset. Out of all of the models we tested, we achieved the best result of 92.9% with sentence embeddings output by BERT as fea- tures as well as a bag-of-words that were fed into a simple forward-feed neural network, using an end-to-end embedding and classi- fication method.

For full writeup: `CIS530_Final_Project.pdf`.
For presentation slides: `presentation.pptx`.

## Models
A variety of models are used in this project:
- Random forest, XGBoost and multi-layer perceptron using bag of words (BOW) as feature - `BOW_sklearn_models.ipynb`.
- BERT only - `BERT_only.ipynb`.
- BERT embeddings with BOW as features to sklearn models - `BERT_Embeddings_sklearn_models.ipynb`.
- BERT embeddings chained as input with BOW to separate neural network - `BERT_BOW_Separate.ipynb`.
- End-to-end classifcation with BERT-as-a-layer in neural network with BOW - `BERT_BOW_Combined.ipynb`.

## Data
Raw dataset can be found in `datasets/C50/`. 

Within the `datasets/` folder are additional processed data files. These are saved and reloaded for convenience to save time from re-processing the raw data on each run of the code.

- `train_x.p, train_y.p, test_x.p, test_y.p`: Train/test data fit for sklearn models.
- `reuters50_train.pkl, reuters50_test.pkl`: Train/test data fit for pytorch/BERT.
- `text_bow_train.p, text_bow_test.p`: Train/test bag of words.
