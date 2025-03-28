# chd-prediction-keras
Neural network-based binary classification of Coronary Heart Disease (CHD) using the UCI Cleveland Heart Disease dataset.
# 🫀 Coronary Heart Disease (CHD) Prediction Using Neural Networks

This project uses a **binary-class Neural Network classifier** built with **Keras** to predict the presence of Coronary Heart Disease (CHD) based on patient diagnostic data from the Cleveland Heart Disease dataset.

##  Dataset
- **Source**: [UCI Machine Learning Repository - Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/heart+disease)
- **Attributes**: 13 features + 1 target column (`num`)
- **Target Conversion**: 
  - `num = 0` → No CHD (label `0`)
  - `num = 1–4` → CHD present (label `1`)
- A new binary column `binary_num` was created and used as the target variable.

##  Key Steps

1. **Data Loading**
   - Dataset loaded from Google Drive using `pandas`.

2. **Preprocessing**
   - Converted `num` column to binary `binary_num`.
   - One-hot encoded categorical variables.
   - Normalized numerical features using `StandardScaler`.

3. **Model Training**
   - Split data into 80% training, 20% testing.
   - Used an 80/20 train-validation split for training.
   - Neural network architecture:
     - Input layer with 16 neurons (ReLU)
     - Hidden layer with 8 neurons (ReLU)
     - Output layer with 1 neuron (Sigmoid)
   - Loss function: `binary_crossentropy`
   - Optimizer: `adam`
   - Evaluation metric: `accuracy`

4. **Overfitting Detection**
   - Validation loss increased after ~20 epochs.
   - Plotted training vs. validation loss to visualize overfitting.

5. **Evaluation**
   - Predictions made on the test set.
   - Performance reported using `classification_report` (precision, recall, F1-score).

## 📊 Results

- **Model showed signs of overfitting** beyond ~20 epochs.
- Suggested improvements:
  - Add Dropout layers
  - Use EarlyStopping
  - Reduce number of epochs

##  Libraries Used
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `keras` (TensorFlow backend)

##  How to Run

1. Clone the repo or open in Google Colab
2. Mount Google Drive and update dataset path
3. Run all cells sequentially

## 🔍 Files
- `heart_disease.csv` → Dataset (uploaded to Google Drive)
- `chd_neural_network.ipynb` → Jupyter notebook (main script)
- `README.md` → This file

---

##  Author

**Tsegie Kassahun**  
Health Informatics & Data Science | Military Veteran | Occupational Therapist  
[LinkedIn](#) | [GitHub](#)

