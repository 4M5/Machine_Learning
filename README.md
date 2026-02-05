# Machine Learning

This repository contains a collection of Jupyter Notebooks demonstrating various machine learning algorithms and techniques. Each notebook focuses on a specific model or concept, providing practical examples and implementations.

## 📚 Notebooks

* 🔹**[DBSCAN.ipynb](DBSCAN.ipynb)**:
    *   **Description**: Implementation of Density-Based Spatial Clustering of Applications with Noise (DBSCAN). This notebook explores how to cluster data based on density, identifying core samples and outliers.
    *   **Key Concepts**:
        *   **Density vs. Distance**: Unlike K-Means (which uses distance to centroids), DBSCAN groups points based on density (how closely packed they are). This allows it to find clusters of arbitrary shapes (like moons or rings).
        *   **Parameters**:
            *   `eps` (Epsilon): The maximum distance between two samples for one to be considered as in the neighborhood of the other.
            *   `min_samples`: The number of samples (or total weight) in a neighborhood for a point to be considered as a core point.
        *   **Point Types**:
            *   *Core Point*: Has at least `min_samples` neighbors within `eps`.
            *   *Border Point*: Within `eps` of a core point but has fewer than `min_samples` neighbors.
            *   *Noise Point*: Not a core point and not close enough to one. Labeled as `-1`.

* 🔹**[Kmeans.ipynb](Kmeans.ipynb)**:
    *   **Description**: Demonstration of the K-Means clustering algorithm. It covers data partitioning into K distinct clusters driven by centroids.
    *   **Key Concepts**:
        *   **Centroid-Based**: The algorithm works by iteratively updating `k` center points (centroids).
        *   **The Process**:
            1.  **Initialize**: Pick `k` random points as starting centroids.
            2.  **Assign**: Every data point joins the team of the closest centroid.
            3.  **Update**: Recalculate centroids as the average position of all team members.
            4.  **Repeat**: Steps 2 and 3 until the centroids stop moving (convergence).
        *   **Strength/Weakness**: Fast and efficient for simple, round clusters. Struggles with complex shapes (use DBSCAN for those).

* 🔹**[Linear_Regression.ipynb](Linear_Regression.ipynb)**:
    *   **Description**: A basic example of a Linear Regression model. It demonstrates fitting a linear equation to observed data using the `scikit-learn` library.
    *   **Key Concepts**:
        *   **The Goal**: Find the "Line of Best Fit" that runs through the data points with minimal error.
        *   **Formula**: `y = mx + b` (or `y = w*x + c` in ML terms).
            *   `x`: Input feature.
            *   `y`: Target to predict.
            *   `w` (Slope/Weight): How much `y` changes when `x` changes.
            *   `c` (Intercept): The baseline value of `y` when `x` is 0.
        *   **Use Case**: Predicting continuous values like house prices, temperature, or sales figures.

* 🔹**[Perceptron_Model.ipynb](Perceptron_Model.ipynb)**:
    *   **Description**: Implementation of the Perceptron algorithm, one of the simplest types of artificial neural networks used for binary classifiers.
    *   **Key Concepts**:
        *   **The "Artificial Neuron"**: It takes multiple inputs, multiplies them by weights, sums them up, and passes the result through an activation function.
        *   **Decision Boundary**: It essentially draws a straight line (or plane) to separate two classes of data (e.g., Cats vs. Dogs).
        *   **Limit**: It is a "Linear Classifier", meaning it can only solve problems where data can be separated by a straight line. It fails on complex patterns (like XOR problems), which is why we use Multi-Layer Perceptrons (Neural Networks) today.

* 🔹**[Regression.ipynb](Regression.ipynb)**:
    *   **Description**: General regression analysis examples, potentially exploring different regression techniques or datasets.
