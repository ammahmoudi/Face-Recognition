# Face Classification by SVM on Eigenfaces

We are going to build a classifier (Face recognition using Eigen faces, PCA and support vector machines) to distinguish the faces of 40 people on a toy dataset. The dataset includes 400 pictures of 40 people faces, each by a 64*64 pixel picture.

![samples of data](/samples.png)
## Code Explanation

### **Dataset and Visualization**:
- The dataset consists of **400 pictures** of **40 people's faces**, each represented by a **64x64 pixel image**.
- The code visualizes the first image of each class (person) using subplots.

### **Train-Test Split**:
- The data is split into train and test sets with a **70% train** and **30% test** split.
- Dimensions of the sets are printed.

### **Dimensionality Reduction (PCA)**:
- Principal Component Analysis (PCA) is used to reduce dimensionality.
- The number of components is chosen to keep **90% variance**.
- Scree plot shows the proportion of variance explained by each component.

### **Eigenfaces Visualization**:
- Eigenfaces are the top eigenvectors from PCA.
- The first 30 eigenfaces are plotted, showing facial features.

    ![samples of data](/eigen.png)

### **Transforming Data with PCA**:
- Train and test features are transformed using PCA.

### **SVM Classifier Training**:
- An SVM classifier is trained on the transformed data.
- Grid search is used for hyperparameter tuning.

### **Model Evaluation**:
- Model predictions are checked on test samples.
- Precision-Recall tradeoff is visualized.
- Decision threshold where recall equals precision is determined.

### **ROC/AUC Comparison**:
- A Random Forest classifier with 30 estimators is trained.
- ROC curve and AUC are calculated for both SVM and Random Forest.
- SVM has an AUC of 0.98, indicating good performance.

### **Classification Report and Confusion Matrix**:
- Classification report shows precision, recall, and F1-score for each class.
- Confusion matrix visualizes true/false classifications per class.
