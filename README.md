# A simple baseline algorithm for graph classification

This repository proposes an implementation of the work developped and presented in: https://arxiv.org/abs/1810.09155

### Abstract

Graph classification has recently received a lot of attention from various fields of machine learning e.g. kernel methods, sequential modeling or graph embedding. All these approaches offer promising results with different respective strengths and weaknesses. However, most of them rely on complex mathematics and require heavy computational power to achieve their best performance. We propose a simple and fast algorithm based on the spectral decomposition of graph Laplacian to perform graph classification and get a first reference score for a dataset. We show that this method obtains competitive results compared to state-of-the-art algorithms. 

### Method

<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/method_schema.png" width="1000">


### Results




### Additional results

<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/results.png" width="1000">
##### Accuracy (%) of serveral classifiers combined to spectral features embedding

Several experiments has been done with adidtional classifiers: random forest classifier (RFC), $k$-nearest neighbors classifier ($k$-NNC), 2-layers perceptron with Relu non-linearity (MLP), support vector machine with \textit{one versus one} classification (SVM) and ridge regression classifier (RRC).


<img src="https://github.com/edouardpineau/A-simple-baseline-algorithm-for-graph-classification/raw/master/images/k_dependence.png" width="1000">
##### Accuracy (%) of RF combined to the spectral features embedding of different dimensions

A single dataset is archived in the DATASETS file, others can be found here: https://ls11-www.cs.tu-dortmund.de/staff/morris/graphkerneldatasets
