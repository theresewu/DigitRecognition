The task of this project is to predict the digit an image represents among 10 possible classes 0-9. Using scikit-learn, an estimator for classification is a Python object that implements the methods fit(X, y) and predict(T). The estimator we adopt here is the class sklearn.svm.SVC that implements support vector classification. 

We conduct SVM experiments with various parameters, and also tested against our own digit drawing from pixels, then rewrite as 8 x 8 matrices. And then reconstruct it to make sure it returns the expected image. The initial learning data set was obtained from Pen-Based Recognition of Handwritten Digits Data Set. The data set was collected from 30 writers who were asked to write 250 digits in random order inside boxes of 500 x 500 tablet pixel resolution. Each screen contains five boxes with the digits to be written displayed above at fixed time intervals of 100 miliseconds inside these boxes, and the first ten digits are ignored.

To represent digits as constant length feature vectors, the data is resampled at (x_t, y_t) points represented as a sequence of T points (x_t, y_t), t = 1, ..., T, and the scientists collected the datasets determines T=8 gave the best trade-off between accuracy and complexity.

dataset is a dictionary-like object that holds all the data and some metadata about the data imported from sklearm to digits. Then digits.items() returns the information about the data:

    dict_items([('images', array(1979 8 x 8 arrays)), 
                ('target_names', array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])),
                ('data', array(1979 64 x 1 arrays)), 
                ('DESCR', "Information about data"), 
                ('target', array([0, 1, 2, ..., 8, 9, 8]))])
