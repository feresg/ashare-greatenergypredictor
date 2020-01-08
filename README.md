## ASHARE - Great Energy Predictor

### Libraries used
*   Pandas and Numpy
*   Plotting libraries (Matplotlib and Seaborn)
*   SkLearn for preprocessing (LabelEncoder), train_test_split and performing Hyperparameter Tuning
*   lightgbm for testing gradient boosting ML model on dataset
*   Keras in Tensorflow for creating and training the Neural Network model

### Steps in notebook
*   Downloading the dataset via Kaggle CLI and loading into Pandas DataFrames
*   **Exploaratory data analysis:** Plotting distrubutions, checking columns with null values, Checking categorical data value counts, correlation with target variable, plotting skewed features or features with outliers
*   **Data processing pipeline:** for easy transformation of both train and test datasets. Performing data cleaning, replacing null values, label encoding, feature engineering, fixing formats like timestamps, reducing memory usage and merging datasets
*   **Modeling:** Trying LightGBM ML model, building Keras neural network, creating callback for training (early stopping, model saving, reducing learning rate on plateau), training the model and preparing hyperparameter tuning pipleine. Best model saved to h5 file for easy reuse.
*   **Submission:** performing data processing pipeline on test datasets, getting test results and submitting via Kaggle CLI

### Model
Keras Deep Neural Network with layer sizes (512, 256, 128, 64, 32), with dropout and batch normalization and relu activations for all neurons (relu layer in output ensures that the meter_reading prediction is positive), trained using Adam optimizer and a variable learning rate.