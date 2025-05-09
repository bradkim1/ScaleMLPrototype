# ScaleMLPrototype
In this notebook, I developed a scalable fraud detection workflow using a modular Python class capable of handling large datasets. The pipeline encapsulates preprocessing, feature engineering, and model training using RandomForestClassifier, GradientBoostingClassifier, or XGBClassifier, with support for outlier removal, PCA-based dimensionality reduction of high-dimensional V features, and aggregated statistical features.

To prevent memory overload during prediction on large datasets, the workflow supports chunked processing—reading and transforming data in smaller batches to avoid loading the entire dataset into memory at once. This chunk-based approach enables efficient training and inference even in memory-constrained environments like Colab.

For deployment readiness, the pipeline guarantees consistent preprocessing between training and inference and writes predictions—including probabilities—to disk. While this prototype processes training data as full DataFrames, it is structured to be extended easily for streaming or distributed prediction scenarios with minimal changes.

Original datasets source: https://www.kaggle.com/competitions/ieee-fraud-detection/data

Data file used in this notebook: https://drive.google.com/drive/folders/1XVqZ1psVwXygFlhLsOjvrhm9XM0wKlQ2?dmr=1&ec=wgc-drive-globalnav-goto
