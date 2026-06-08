# A-VISS-CNN-LSTM-Research

Research repository for nurse stress classification using multimodal physiological sensor data and a Subject-Dependent CNN-LSTM architecture.

This repository contains the complete research pipeline developed as part of an undergraduate thesis in Information Systems at Hasanuddin University. The study explores the use of deep learning techniques for stress classification based on wearable physiological sensor data collected from nurses in clinical environments.

## Research Title

**Rancang Bangun Prototype A-VISS untuk Klasifikasi Stres Perawat Menggunakan Pendekatan Subject-Dependent CNN-LSTM**

## Research Overview

Stress among healthcare professionals can negatively affect decision-making, productivity, and overall well-being. This research proposes **A-VISS (Automated Vital Intelligence for Stress Surveillance)**, a prototype system that utilizes physiological signals and deep learning techniques to classify stress levels automatically.

The proposed approach employs a **Subject-Dependent CNN-LSTM architecture**, allowing the model to learn individual physiological patterns more effectively than traditional Subject-Independent approaches.

## Dataset

**Nurse Stress Prediction Wearable Sensors Dataset**

Source:
[https://www.kaggle.com/datasets/seyedmajidhosseini/nurse-stress-prediction-wearable-sensors](https://www.kaggle.com/datasets/priyankraval/nurse-stress-prediction-wearable-sensors/data)

Physiological signals used:

* Heart Rate (HR)
* Electrodermal Activity (EDA)
* Skin Temperature (TEMP)
* Accelerometer X
* Accelerometer Y
* Accelerometer Z

## Research Workflow

1. Data Cleaning
2. Signal Interpolation
3. Per-Subject Standardization
4. Sliding Window Segmentation (Window = 60, Step = 5)
5. 3D Tensor Construction
6. CNN-LSTM Model Training
7. Model Evaluation
8. Performance Comparison
9. Dashboard Deployment

## Experimental Scenarios

The study evaluates four experimental configurations:

| Scenario               | Description                    |
| ---------------------- | ------------------------------ |
| Multiclass Independent | Subject-Independent, 3 Classes |
| Multiclass Dependent   | Subject-Dependent, 3 Classes   |
| Binary Independent     | Subject-Independent, 2 Classes |
| Binary Dependent       | Subject-Dependent, 2 Classes   |

## Best Model

**Binary Subject-Dependent CNN-LSTM**

Performance:

* Accuracy: **85%**
* Weighted F1-Score: **86%**

The Binary Subject-Dependent configuration consistently outperformed the other experimental scenarios and was selected for deployment in the A-VISS dashboard prototype.

## Repository Structure

```text
A-VISS-CNN-LSTM-Research/
│
├── notebooks/
│   └── A_VISS_Stress_Prediction_Test.ipynb
│
├── models/
│   └── model_binary_subject_dependent.keras
│
├── figures/
│   ├── workflow.png
│   ├── sliding_window.png
│   ├── cnn_lstm_architecture.png
│   ├── accuracy_loss_curve.png
│   ├── confusion_matrix_binary_dependent.png
│   └── performance_comparison.png
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

## Technologies

* Python
* TensorFlow / Keras
* NumPy
* Pandas
* Scikit-Learn
* Matplotlib
* Plotly
* Google Colab

## Related Repository

Deployment Prototype:

[**A-VISS Project**](https://github.com/Jnxx02/AVISS_Project)

A Streamlit-based dashboard for interactive stress monitoring and visualization using the trained Subject-Dependent CNN-LSTM model.

## License

This project is released under the MIT License.

## Author

[Jonathan Kwan](https://github.com/Jnxx02)

Information Systems
Faculty of Mathematics and Natural Sciences
Hasanuddin University
