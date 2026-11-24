# ☀️ Solar Power Generation Prediction Using Artificial Neural Networks (ANN)

## 📌 Project Overview

This project focuses on predicting solar power generation using an **Artificial Neural Network (ANN)**. It uses historical solar generation data and weather sensor data to estimate AC power output based on environmental and time-related conditions.

The project uses Python, TensorFlow/Keras, Scikit-learn, and Streamlit to develop and demonstrate a deep-learning-based solar power prediction system.

## 🎯 Objectives

- Analyze solar power generation using historical datasets.
- Understand the relationship between weather conditions and solar power output.
- Clean, process, and combine generation and weather datasets.
- Develop an Artificial Neural Network model.
- Predict AC power using weather and time-related features.
- Evaluate model performance using regression metrics.
- Build an interactive prediction interface using Streamlit.

## 📂 Dataset Description

The project uses the **Solar Power Generation Data** dataset from Kaggle.

Two datasets are used:

1. `Plant_1_Generation_Data.csv`
2. `Plant_1_Weather_Sensor_Data.csv`

**Dataset details:**
- Generation records: 68,778
- Weather records: 3,182
- Combined records: 3,157
- Missing values: 0 (reported in source datasets)
- Duplicate records: 0 (reported in source datasets)

Dataset Link: https://www.kaggle.com/datasets/anikannal/solar-power-generation-data

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Model development |
| Pandas | Data processing |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Scikit-learn | Data scaling and evaluation |
| TensorFlow / Keras | ANN model development |
| Streamlit | Interactive web interface |
| Cloudflared | Temporary application access |

## ⚙️ Project Methodology

1. Load generation and weather datasets.
2. Inspect and clean the data.
3. Convert timestamps into datetime format.
4. Aggregate and merge datasets using timestamps.
5. Perform feature engineering.
6. Split data into training and testing sets chronologically.
7. Apply StandardScaler to input features.
8. Build and train the ANN model.
9. Evaluate model performance.
10. Develop an interactive Streamlit application.

## 🧠 ANN Model Architecture

The Artificial Neural Network contains:

- **Input Layer:** 6 features
- **Hidden Layer 1:** 64 neurons (ReLU)
- **Hidden Layer 2:** 32 neurons (ReLU)
- **Output Layer:** 1 neuron (Linear)

**Model Configuration:**
- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Evaluation Metric: Mean Absolute Error (MAE)
- Total Trainable Parameters: 2,561
- Training Epochs: Up to 100
- Batch Size: 32

### Input Features

1. Solar Irradiation
2. Ambient Temperature
3. Module Temperature
4. Hour Sine (HOUR_SIN)
5. Hour Cosine (HOUR_COS)
6. Day of Year

**Prediction Target:** AC_POWER

## 📊 Experimental Results

The model was evaluated using 632 testing samples.

| Evaluation Metric | Result |
|---|---:|
| MAE | 533.253 kW |
| MSE | 816,369.188 (kW)² |
| RMSE | 903.532 kW |
| R² Score | 0.987 |

The model achieved an R² score of **0.987** on the selected chronological test dataset.

## 💻 Application Interface

The project includes a Streamlit application that allows users to enter:

- Solar Irradiation
- Ambient Temperature
- Module Temperature
- Hour of Day
- Day of Year

After entering the values, users can click the **Predict Solar Power** button to obtain an estimated AC power output in kilowatts.

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/solar-power-generation-prediction.git
```

### 2. Open the Project Folder

```bash
cd solar-power-generation-prediction
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow streamlit
```

### 4. Download the Dataset

Download the Solar Power Generation Data from Kaggle and place the required Plant 1 CSV files in the appropriate project directory.

### 5. Run the Application

After placing the Streamlit application and saved model files in the project folder, run:

```bash
streamlit run app.py
```

*Note: Replace `app.py` with your actual Streamlit application filename if it is different.*

## 🔮 Future Scope

- Use larger datasets covering multiple seasons.
- Test the model on additional solar power plants.
- Include more weather and operational parameters.
- Compare ANN with other machine-learning algorithms.
- Improve prediction accuracy and model reliability.
- Deploy the application using permanent cloud hosting.
- Add uncertainty estimates to predictions.

## ⚠️ Limitations

- The dataset covers approximately one month.
- Only Plant 1 historical data is used.
- Some factors, such as cloud cover, shading, maintenance, and inverter status, are not included.
- Model performance is evaluated using one chronological train/test split.
- Predictions are estimates and are not guaranteed future measurements.

## 👨‍💻 Project Information

**Project Title:** Solar Power Generation Prediction Using Artificial Neural Networks (ANN)

**Course:** Artificial Intelligence and Deep Learning

**University:** SR University, Warangal

**Academic Year:** 2026–2027

**Submitted By:** J Vishnu Sharan

**Roll Number:** 2403A510A2

**Project Supervisor:** Anurodh Kumar Sir

## 📚 References

- [Kaggle – Solar Power Generation Data](https://www.kaggle.com/datasets/anikannal/solar-power-generation-data)
- [Python Documentation](https://docs.python.org/3/)
- [TensorFlow Documentation](https://www.tensorflow.org/)
- [Keras Documentation](https://keras.io/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Streamlit Documentation](https://docs.streamlit.io/)

---

## ⭐ Conclusion

This project demonstrates how Artificial Neural Networks can be used to estimate solar power generation using historical generation and weather data. The developed model achieved an R² score of 0.987 on the selected test dataset and was connected to a Streamlit interface for interactive predictions.

**Thank You! ☀️**
