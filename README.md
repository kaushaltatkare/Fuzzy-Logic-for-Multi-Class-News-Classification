# Fuzzy Logic for Multi-Class News Classification

MSc Data Science dissertation by **Kaushal Tatkare**, completed at **Manchester Metropolitan University**.

This project investigates fuzzy logic for news classification using the HuffPost News Category Dataset. It compares conventional machine learning models with Type-1 and Interval Type-2 fuzzy classifiers.

## My Contribution

I independently wrote the code for the Type-1 and Interval Type-2 fuzzy classifiers and evaluated their performance on multi-class news classification.

## Dataset

* **209,527 news articles**
* **42 categories**
* Input text: article headlines and short descriptions
* Class imbalance ratio: approximately **35.1:1**

## Methods

* Text preprocessing: lowercasing, contraction expansion, punctuation removal, spelling correction, stop-word removal and lemmatisation
* TF-IDF feature extraction and Truncated SVD dimensionality reduction
* Naive Bayes, Linear SVM and Logistic Regression baselines
* Type-1 and Interval Type-2 fuzzy classification
* Word2Vec document representations
* WordNet-based grouping of categories
* Evaluation using accuracy, macro precision, macro recall, macro F1 and weighted F1

## Results

| Model                                                  | Accuracy on the original 42-class task |
| ------------------------------------------------------ | -------------------------------------: |
| Logistic Regression with TF-IDF                        |                                 60.12% |
| Linear SVM with TF-IDF                                 |                                 59.75% |
| Naive Bayes with TF-IDF                                |                                 51.15% |
| Type-1 fuzzy classifier with TF-IDF/SVD                |                                 24.49% |
| Tuned Interval Type-2 fuzzy classifier with TF-IDF/SVD |                                 24.07% |

Word2Vec-based fuzzy classification achieved **28.77% accuracy**.

Classification over **10 WordNet-based category groups** achieved **49.66% accuracy**. This is a simpler task than classification across 42 categories, so the results are not directly comparable.

## Findings and Limitations

The implemented fuzzy classifiers did not outperform the conventional baselines on the original 42-class task.

The initial fuzzy classifiers used 20,000 training instances, while the conventional baselines used 167,621. This difference limits the comparison.

The experiments examine how feature representation, class imbalance, training-set size and category grouping affect classification performance.

## Repository Contents

* Jupyter notebook containing the implementation and saved experiment results
* Dissertation report describing the research, methods, results and limitations

## Running the Notebook

Download the HuffPost News Category Dataset separately and update the dataset path in the notebook. Install the required Python packages and language resources used in its setup cells, then run the notebook in order.

## Author

**Kaushal Tatkare**

[LinkedIn](https://www.linkedin.com/in/kaushaltatkare07/) · [GitHub](https://github.com/kaushaltatkare)

