# 🌸 Flower Image Clustering with K-Means 🌸

## Introduction

This repository features a Jupyter Notebook dedicated to clustering flower images using machine-learning techniques. The primary objective of this project is to explore how visual features extracted from images can be utilized to group similar flowers through K-means clustering. By leveraging the power of deep learning, specifically the VGG16 convolutional neural network, we aim to demonstrate the effectiveness of feature extraction in image classification tasks.

![Flower Clustering](https://github.com/MJParviz/Flower_Image_Clustering_with_Transfer_Learning_and_K-Means/blob/main/0001.png)

## Methodology

### Data Preparation

The project begins with loading a dataset containing flower images and their corresponding labels. The dataset is structured such that each image file is accompanied by a label in a CSV file. This setup allows us to easily access the images and their classifications.

### Feature Extraction

To extract meaningful features from the images, we utilize the VGG16 model, a popular convolutional neural network known for its impressive performance in image classification tasks. We load the model without the top fully connected layers, enabling us to obtain high-level feature representations of the input images. Each image is resized to the VGG16 input dimensions, preprocessed, and then passed through the model to extract features.

### Dimensionality Reduction

Given that the feature vectors can be high-dimensional, we apply Principal Component Analysis (PCA) to reduce the dimensionality of the data. This step allows us to visualize the data more effectively and facilitates the clustering process.

### Clustering with K-Means

With the reduced feature set, we implement the K-Means clustering algorithm. The choice of the optimal number of clusters (K) is determined using the elbow method, which involves plotting the inertia (within-cluster sum of squares) against different values of K. Once the optimal K is identified, we fit the K-Means model and assign cluster labels to the images.

### Evaluation

To evaluate the clustering performance, we calculate the silhouette score and homogeneity score. The silhouette score measures how similar an object is to its cluster compared to other clusters, while the homogeneity score assesses how closely the clusters correspond to the actual labels.

## Results

The notebook presents various visualizations, including the elbow method plot, which aids in selecting the optimal number of clusters. Additionally, scatter plots display the clustered data in the PCA-reduced space, providing insights into the clustering behavior. The evaluation metrics offer a quantitative assessment of the clustering quality.

![Elbow Method Plot](https://github.com/MJParviz/Flower_Image_Clustering_with_Transfer_Learning_and_K-Means/blob/main/elbow.png)

## Conclusion

In this project, we explored the process of clustering flower images using a transfer learning approach with the VGG16 model for feature extraction. While the use of deep learning techniques like VGG16 can be powerful, it may not be the best fit for our specific clustering problem. The complexities introduced by the model's architecture and the high dimensionality of the features could complicate the clustering process. Future work might focus on simpler feature extraction methods or different clustering algorithms to better suit the nature of the data and improve clustering performance.

## 📁 Project Content

- **`flower_clustering_notebook.ipynb`**: The main Jupyter Notebook containing all code and visualizations.
- **`flower_labels.csv`**: The dataset containing image paths and labels.
- **`flower images`**: A package of images.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Happy clustering! 🌼
