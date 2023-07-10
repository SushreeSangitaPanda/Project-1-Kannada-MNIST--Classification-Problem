# Project-1-Kannada-MNIST--Classification-Problem
Problem Statement: This is an extension of clasic MNIST classification problem. Instead of using Hindu numerals, lets use a recently-released dataset of Kannada digits. This is a 10 Class classification problem.
# Data :
The dataset used in the project is from Kaggle.
Dataset can be downloaded from the link : https://www.kaggle.com/datasets/higgstachyon/
kannada-mnist.
## A step-by-step explanation of the code for the classification problem using Kannada MNIST dataset and generating various visualizations:
1. Import the required libraries:
   - The necessary libraries are imported to perform the classification task, including numpy, matplotlib, seaborn, sklearn, yellowbrick, and PdfPages.

2. Load the dataset:
   - The dataset is loaded from the .npz file using numpy's 'load()' function. The training and testing data along with their respective labels are assigned to variables.

3. Define helper functions:
   - Two helper functions are defined:
     - 'generate_metrics_bar_chart()': This function takes model name, precision, recall, and F1-score as inputs and generates a bar chart visualization using matplotlib to represent these metrics.
     - 'generate_confusion_matrix_heatmap()': This function generates a confusion matrix heatmap using the Yellowbrick library for a given model, input data, and labels.

4. Perform PCA and evaluate models:
   - A list of component sizes is defined.
   - A loop is executed for each component size:
     - The images are flattened, and PCA is performed using the specified component size.
     - Each model (Decision Trees, Random Forest, Naive Bayes, KNN, SVM) is trained and evaluated using the transformed data.
     - Classification metrics (precision, recall, F1-score) are computed for each model and displayed using the 'generate_metrics_bar_chart()' function.
     - A confusion matrix heatmap is generated for each model using the 'generate_confusion_matrix_heatmap()' function.
     - RoC - AUC curves are plotted for each model using the Yellowbrick library.

5. Save metrics, confusion matrix, and RoC - AUC curve to PDF files:
   - For each component size, a separate PDF file is created to store the visualizations.
   - For each model, the metrics bar chart, confusion matrix heatmap, and RoC - AUC curve are saved to the respective PDF file using the `savefig()` method from PdfPages.

6. Combine individual PDF files into a single PDF file:
   - All the individual PDF files are combined into a single PDF file named "classification_results.pdf".
   - A PdfPages object is created to write the combined PDF file.
   - For each individual PDF file, the pages are extracted and saved into the combined PDF file.
   - 
# Conclusion
This code performs the classification problem on the Kannada MNIST dataset, generates various visualizations, and saves them into PDF files for each component size. Finally, it combines all the individual PDF files into a single PDF file for easy reference.
Make sure to adjust the filename and paths according to your specific requirements and have the necessary packages installed.
