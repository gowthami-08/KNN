KNN (K-Nearest Neighbors) is a supervised machine learning algorithm used for classification and regression.
It predicts the label of a data point based on the majority class of its 'K' nearest neighbors in the training set.

 KNN algorithm working-
-Choose a value for K (number of neighbors).
-For a new data point:
-Measure the distance (usually Euclidean) to all other points in the training data.
-Find the K closest points.
-Use majority voting from those neighbors to classify the new point.

KNN sensitive to noise? Yes, KNN is sensitive to noise:
If noisy or misclassified data is nearby, it may wrongly influence predictions.
This is especially true for small K values (e.g., K=1), which rely heavily on just one neighbor.

We tested K from 1 to 10: That means we evaluated 10 different K values. We used validation accuracy
For each K, we checked how well the model predicted on the validation set using. Then, we plotted K vs accuracy and selected the K with the highest accuracy and we got the test accuracy of 1.0 and the validation accuracy as 0.97

Decision Boundary?
A decision boundary is a line or surface that separates classes in the feature space. In classification, it shows where the model predicts one class vs. another.
In your case (Iris dataset), the KNN classifier creates a non-linear boundary based on distance to neighbors. The plot helps us visualize how the KNN model classifies different regions in the feature space.

Why are we using PCA here-
The Iris dataset has 4 features (sepal length, sepal width, petal length, petal width).We cannot directly visualize 4D space.So, we apply PCA (Principal Component Analysis) to reduce the dimensions to 2D.
This allows us to plot the data and visualize the decision boundary in two dimensions.

Summary-
PCA is used to convert the high-dimensional data into 2D, so it can be visualized.
The decision boundary shows where the KNN model switches between class predictions.
This plot helps us understand how well the model separates the classes, and how confident or confused it may be in some regions.
