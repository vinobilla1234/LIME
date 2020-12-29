# LIME
This project is about explaining what machine learning classifiers (or models) are doing. At the moment, we support explaining individual predictions for text classifiers or classifiers that act on tables (numpy arrays of numerical or categorical data) or images, with a package called lime (short for local interpretable model-agnostic explanations). Lime is based on the work presented in this paper (bibtex here for citation). Here is a link to the promo video:

KDD promo video

Our plan is to add more packages that help users understand and interact meaningfully with machine learning.

Lime is able to explain any black box classifier, with two or more classes. All we require is that the classifier implements a function that takes in raw text or a numpy array and outputs a probability for each class. Support for scikit-learn classifiers is built-in.

Installation
The lime package is on PyPI. Simply run:

pip install lime
Or clone the repository and run:

pip install .
We dropped python2 support in 0.2.0, 0.1.1.37 was the last version before that.

Screenshots
Below are some screenshots of lime explanations. These are generated in html, and can be easily produced and embedded in ipython notebooks. We also support visualizations using matplotlib, although they don't look as nice as these ones.

Two class case, text
Negative (blue) words indicate atheism, while positive (orange) words indicate christian. The way to interpret the weights by applying them to the prediction probabilities. For example, if we remove the words Host and NNTP from the document, we expect the classifier to predict atheism with probability 0.58 - 0.14 - 0.11 = 0.31.

twoclass

Multiclass case
multiclass

Tabular data
tabular

Images (explaining prediction of 'Cat' in pros and cons)
