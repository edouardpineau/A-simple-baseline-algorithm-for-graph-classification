# A simple baseline algorithm for graph classification

This repository proposes an implementation of the work developped and presented in: https://arxiv.org/abs/1810.09155

### Abstract

Graph classification has recently received a lot of attention from various fields of machine learning e.g. kernel methods, sequential modeling or graph embedding. All these approaches offer promising results with different respective strengths and weaknesses. However, most of them rely on complex mathematics and require heavy computational power to achieve their best performance. We propose a simple and fast algorithm based on the spectral decomposition of graph Laplacian to perform graph classification and get a first reference score for a dataset. We show that this method obtains competitive results compared to state-of-the-art algorithms. 

### Method

<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/method_schema.png" width="700">
Figure 1: Schematic view of our model. L denotes the normalized Laplacian of the graph, c the predicted class. 

### Results

<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/results.png" width="700">
Table 1: Experimental accuracy (%) of different models plus ours over standard molecular datasets.

### 

As we can see, RFC provides the best results for all datasets except DD where MLP has an accuracy of 75.6 against 75.4. Our intuition to explain these good results is that the decision tree classifier, which is at the core of RFC, is an algorithm based on level thresholding. Our paper uses [1] to say that the spectral features represent a sequence of energy levels. With this intuition, being above or below a certain level is thus likely to be meaningful for classification.

### Additional results

<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/additional_results.png" width="700">
Table 2: Accuracy (%) of different classifiers combined to the spectral features embedding.

### 

Several experiments has been done with adidtional classifiers: random forest classifier (RFC), k-nearest neighbors classifier (k-NNC), 2-layers perceptron with Relu non-linearity (MLP), support vector machine with \textit{one versus one} classification (SVM) and ridge regression classifier (RRC).

### 

<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/k_dependence.png" width="1000">
Table 3: Accuracy (%) of RF combined to the spectral features embedding of different dimensions.


[1] Thomas Bonald, Alexandre Hollocou, and Marc Lelarge. Weighted spectral embedding of graphs. arXiv preprint arXiv:1809.11115, 2018.

A single dataset is archived in the DATASETS file, others can be found here: https://ls11-www.cs.tu-dortmund.de/staff/morris/graphkerneldatasets
