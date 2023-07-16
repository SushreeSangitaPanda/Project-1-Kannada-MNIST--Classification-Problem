# Project-1-Kannada-MNIST--Classification-Problem
Problem Statement: This is an extension of clasic MNIST classification problem. Instead of using Hindu numerals, lets use a recently-released dataset of Kannada digits. This is a 10 Class classification problem.
# Data :
The dataset used in the project is from Kaggle.
Dataset can be downloaded from the link : https://www.kaggle.com/datasets/higgstachyon/
kannada-mnist.
## A step-by-step explanation of the code for the classification problem using Kannada MNIST dataset and generating various visualizations

1. Imports necessary libraries and modules:
   - `pandas` for data manipulation and analysis
   - `os` for file operations
   - `matplotlib.backends.backend_pdf.PdfPages` for generating PDF files
   - `sklearn` modules for classification models and evaluation metrics
   - `seaborn` for visualization
   - `yellowbrick` for ROC-AUC curve visualization
   - `PyPDF2.PdfMerger` for merging PDF files

2. Defines the list of classification model names and component sizes.

3. Initializes dictionaries to store precision, recall, and F1-score for each model.

4. Defines a function, `get_classifier()`, to return the appropriate classifier based on the given model name.

5. Defines a function, `calculate_metrics()`, to calculate precision, recall, and F1-score for the given true and predicted labels.

6. Loops over each component size:
   - Flattens the training and test images.
   - Performs PCA with the current component size.
   - Trains and evaluates classification models for each model name:
     - Retrieves the classifier based on the model name.
     - Fits the classifier on the PCA-transformed training data.
     - Predicts the labels for the PCA-transformed test data.
     - Calculates precision, recall, and F1-score using the `calculate_metrics()` function.
     - Stores the metrics in the corresponding dictionaries.
     - Generates metrics bar chart, confusion matrix heatmap, and ROC-AUC curve for the current model:
       - Saves the metrics bar chart as a PDF file.
       - Saves the confusion matrix heatmap as a PDF file.
       - Saves the ROC-AUC curve as a PDF file.

7. Creates a model comparison table:
   - Prepares lists for each metric (model name, precision, recall, and F1-score).
   - Populates the lists with the metrics for each model and the current component size.
   - Constructs a pandas DataFrame using the populated lists.

8. Saves the model comparison table as a PDF file.

9. Combines all the individual PDF files into a single PDF file:
   - Initializes a `PdfMerger` object.
   - Appends each individual PDF file to the merger.
   - Writes the merged PDF file.

10. Deletes the individual PDF files.

This code allows for the evaluation of classification models using PCA and provides a comprehensive set of PDF reports for each component size. The reports include metrics bar charts, confusion matrix heatmaps, ROC-AUC curves, and a model comparison table. The generated PDF reports can be useful for visualizing and comparing the performance of different classification models with varying component sizes.

# Conclusion
When the PCA component size increases and the precision score also increases, it suggests that including more principal components in the feature representation improves the precision of the models.
The increase in precision with larger PCA component sizes can be interpreted as the models capturing more relevant information from the data, resulting in better discrimination between different classes. By including more principal components, the models have access to additional patterns and variations in the data, leading to more accurate predictions.
