🧠 **Activity Recognition Model – Open Door vs Rub Hands**

This project focuses on recognizing and classifying human activities using time-series sensor data. Specifically, it distinguishes between two common activities — **"Open Door"** and **"Rub Hands"** — using data from **accelerometer** and **gyroscope** sensors. The project involves dataset filtering, preprocessing, feature extraction, model training, and evaluation.

---

## 📂 Dataset Details

The dataset used in this project is a subset of the **BBH dataset**, which contains sensor data collected from wearable devices. From this dataset, we extracted samples for:

### 🔸 Activities:
- `20` → Open Door  
- `36` → Rub Hands  

### 🔸 Sensors:
- Accelerometer  
- Gyroscope  

### 📄 Processed Data Files:
- `trainJinsAccelerometer.npy` – Training accelerometer data  
- `trainJinsGyroscope.npy` – Training gyroscope data  
- `trainLabels.npy` – Labels for training data  
- `testJinsAccelerometer.npy` – Testing accelerometer data  
- `testJinsGyroscope.npy` – Testing gyroscope data  
- `testLabels.npy` – Labels for testing data  

---

## 🚀 How the Project Works

### 1️⃣ Data Extraction (`Data_Extraction.ipynb`)
- Loads the original BBH dataset  
- Filters data to retain only "Open Door" and "Rub Hands" activities  
- Extracts data from accelerometer and gyroscope sensors  
- Saves filtered sensor data as `.npy` files  

### 2️⃣ Model Training & Evaluation (`Activity_Monitoring.ipynb`)
- Loads preprocessed `.npy` files  
- Extracts statistical features (mean, min, max, std, etc.)  
- Trains the following models:
  - Logistic Regression  
  - Neural Network (using Keras)  
- Evaluates model performance using:
  - Accuracy  
  - Confusion Matrix  
  - Precision, Recall, F1-score  

---

## 📈 Results

Both models achieved solid performance in classifying the two activities.  
Key evaluation metrics:
- ✅ **Accuracy**  
- 📊 **Confusion Matrix**  
- 📃 **Classification Report**  

---

## 🛠️ Technologies Used

- Python 3.x  
- NumPy – Numerical computations  
- Pandas – Data processing  
- scikit-learn – ML models and evaluation  
- Matplotlib – Visualizations  
- Keras / TensorFlow – Deep learning models  

---

---

## 🔮 Future Improvements

- Add more activity classes for multiclass classification  
- Use advanced time-series models like LSTM or 1D CNN  
- Improve feature engineering and selection  
- Implement real-time recognition using live sensor input  

---
