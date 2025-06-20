🧠 Activity Recognition Model – Open Door vs Rub Hands

This project focuses on recognizing and classifying human activities using time-series sensor data. Specifically, it distinguishes between two common activities — "Open Door" and "Rub Hands" — using data from accelerometer and gyroscope sensors. The project involves dataset filtering, preprocessing, feature extraction, model training, and evaluation.

Dataset Details

The dataset used in this project is a subset of the BBH dataset, which contains sensor data collected from wearable devices. From this dataset, we extracted samples for:

Two Activities:

20 → Open Door

36 → Rub Hands

Two Sensors:

Accelerometer

Gyroscope

Processed and prefiltered data is saved in .npy files for ease of use during model training.

Files:

trainJinsAccelerometer.npy – Training accelerometer data

trainJinsGyroscope.npy – Training gyroscope data

trainLabels.npy – Labels for training data

testJinsAccelerometer.npy – Testing accelerometer data

testJinsGyroscope.npy – Testing gyroscope data

testLabels.npy – Labels for testing data

How the Project Works

Data Extraction (Data_Extraction.ipynb)

Loads the original BBH dataset

Filters the dataset to keep only the target activities

Separates readings from the Accelerometer and Gyroscope

Saves the filtered sensor data and corresponding labels in .npy format

Model Training and Evaluation (Activity_Monitoring.ipynb)

Loads the processed .npy files

Extracts statistical features (mean, max, min, std, etc.)

Trains the following models:

Logistic Regression

Neural Network (using Keras)

Evaluates the model using:

Accuracy

Classification report (Precision, Recall, F1-score)

Confusion matrix

Results

Both models showed effective performance in classifying the selected activities. Evaluation on the test dataset was conducted using:

Accuracy

Confusion Matrix

Precision, Recall, F1-score

Technologies Used

Python 3.x

NumPy – Numerical computation

Pandas – Data handling

scikit-learn – ML models and evaluation

Matplotlib – Visualization

Keras / TensorFlow – Neural network modeling

Project Structure

Copy
Edit
Activity_Recognition_Model/
├── Data_Extraction.ipynb
├── Activity_Monitoring.ipynb
├── trainJinsAccelerometer.npy
├── trainJinsGyroscope.npy
├── trainLabels.npy
├── testJinsAccelerometer.npy
├── testJinsGyroscope.npy
├── testLabels.npy
└── README.md
Future Improvements

Include more activity classes for multi-class classification

Use time-series models like LSTM or 1D CNN

Apply feature selection techniques

Deploy real-time activity recognition using streaming sensor data
