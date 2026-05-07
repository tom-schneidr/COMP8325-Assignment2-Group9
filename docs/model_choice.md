# Model Choice Rationale

For Assignment 2, we chose to use two supervised tree-based classifiers:

- `DecisionTreeClassifier`
- `RandomForestClassifier`

The assignment requires us to classify BODMAS samples into malware categories, including benign samples. This is a supervised multiclass classification task using tabular feature vectors extracted from executable files. Both selected models are appropriate for this type of structured numeric data.

## Decision Tree Classifier

We selected a Decision Tree classifier as our simpler and more interpretable model. Decision trees were covered in the practical material for supervised classification, so this model stays close to the methods discussed in the unit.

A decision tree learns a sequence of feature-based rules to separate classes. This makes it useful as a baseline because its behaviour is easier to explain than many more complex models. It also gives us a way to observe how well a single tree can separate malware categories using the provided BODMAS features.

The main limitation is that a single decision tree can overfit the training data. It may learn patterns that are too specific to the training split and may generalise poorly to unseen samples.

## Random Forest Classifier

We selected a Random Forest classifier as the stronger ensemble model. A random forest builds many decision trees and combines their predictions. This directly extends the decision tree idea while reducing the risk of overfitting.

Random forests are well suited to tabular datasets and can model nonlinear relationships between features. This matters for malware classification because the difference between malware categories may depend on interactions between multiple extracted features rather than a single simple rule.

Compared with a single decision tree, Random Forest is usually less interpretable, but it often provides better generalisation and more stable performance.

## Why This Pair Works Well

This pair gives us a clear comparison:

- Decision Tree: simple, interpretable, and lecture-aligned.
- Random Forest: more robust ensemble version of the same core idea.

Using both lets us answer a useful project question:

> Does combining many decision trees improve malware category classification compared with using one interpretable decision tree?

This comparison is easy to explain in the report and presentation because both models are related, but they have different strengths and weaknesses.

## Why We Did Not Choose Other Models

We considered k-nearest neighbours because it was used in the supervised learning practicals. However, BODMAS is likely to be relatively large and high-dimensional, making kNN slower and more sensitive to feature scaling and distance behaviour.

We did not choose clustering or anomaly detection methods such as KMeans, Local Outlier Factor, or Isolation Forest because the assignment provides labels and asks for malware category prediction. Those methods are more suitable for unsupervised anomaly detection, not supervised multiclass classification.

We also did not choose XGBoost, LightGBM, or neural networks because they are more complex and less directly tied to the practical material we reviewed. They may perform well, but Decision Tree and Random Forest give a stronger connection to the unit content while still being suitable for the dataset.
