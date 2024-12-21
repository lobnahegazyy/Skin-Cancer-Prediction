I.	Project Description
This project focuses on developing a robust image classification system using machine learning techniques. The dataset, organized into training and testing directories, comprises images across multiple classes. Images are preprocessed through resizing, grayscale conversion, normalization, and feature extraction techniques such as Otsu's thresholding. Exploratory data analysis includes visualization of sample images, grayscale transformations, and pixel intensity histograms.
Three machine learning models—Logistic Regression, Random Forest, and K-Nearest Neighbors—are trained on the preprocessed dataset. The data is flattened and scaled using StandardScaler for improved model performance. Model evaluation is performed using metrics like accuracy scores and classification reports. Random Forest achieves the best performance among the models, with detailed predictions and visualizations highlighting the system's effectiveness.
This work demonstrates the pipeline for creating an efficient and scalable image classification system, with a focus on preprocessing, model training, and performance evaluation. The approach is adaptable for various image datasets, making it a versatile solution for real-world classification tasks.

II.	Methodology 

•	Data Collection: Data is collected from Kaggle, this data consists of 9305 images for training and 200 images for testing. It has 2 labels “Benign and malignant”.
“Benign (0)” for non-cancerous skin.
“Malignant (1)” for cancerous skin.

 
•	Data Preprocessing: It involves essential steps to prepare the images for machine learning models:
a.	Resize: Images are resized to 128x128 pixels to ensure that all images have the same dimensions
b.	Grayscale conversion: Reducing the 3-color channel (RGB) using library skimage (rgb2gray) and making it only one channel, which will help in displaying a histogram distribution.

c.	Normalization: Normalizing the pixels values from 0 to 255 making the training process easy and stable.
d.	Flattening: flattening the images to 1D, it’s necessary for machine learning models.
e.	Scaling: Scaling the dataset using StandardScaler ensures the input pixel values are on similar scale.
f.	Feature Extraction: Applying Otsu’s Thresholding (T) to each image to extract binary features, it divides images into object and background (< T background), (>T Object).

III.	Machine Learning

Machine learning is used to build image classification models. After preprocessing the images, three different machine learning algorithms—Logistic Regression, Random Forest, and K-Nearest Neighbors (KNN)—are applied to train the models and evaluate their performance.

Model	Accuracy
Random Forest	0.90
KNN	0.88
Logistic Regression	0.855

The model with the highest accuracy is Random Forest so it’s used for making predictions.
