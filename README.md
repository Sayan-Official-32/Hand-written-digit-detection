🧠 Handwritten Digit Detection using Deep Learning

A Deep Learning project that classifies handwritten digits (0–9) using a Neural Network built with TensorFlow/Keras.
Achieved ~97–99% accuracy on MNIST-style dataset.

📌 Project Overview

This project implements a multi-class image classification system to recognize handwritten digits from grayscale 28×28 images.

The model is trained using a fully connected neural network (ANN) and evaluated using proper validation techniques to ensure generalization performance.

This project demonstrates:

End-to-end ML pipeline

Data preprocessing

Model training & validation

Performance evaluation

Prediction visualization

Confusion matrix analysis

🏗 Problem Statement

Given an image of a handwritten digit (0–9), the goal is to predict the correct digit class.

This is a multi-class classification problem with 10 output classes.

📊 Dataset

Dataset format:

Total samples: 42,000

Image size: 28 × 28 pixels

Total features per image: 784

Pixel range: 0–255

Dataset structure:

Column	Description
0	Label (0–9)
1–784	Pixel values

If using Kaggle dataset:

Download from:
https://www.kaggle.com/competitions/digit-recognizer

⚙ Data Preprocessing

Steps performed:

Separate features and labels

Convert all values to numeric

Handle missing values

Normalize pixel values:

𝑋
=
𝑋
255
X=
255
X
	​


Reshape into 4D tensor:

(
𝑠
𝑎
𝑚
𝑝
𝑙
𝑒
𝑠
,
28
,
28
,
1
)
(samples,28,28,1)

One-hot encode labels:

𝑦
→
(
𝑠
𝑎
𝑚
𝑝
𝑙
𝑒
𝑠
,
10
)
y→(samples,10)
🧠 Model Architecture

Built using Keras Sequential API.

Input: (28, 28, 1)
↓
Flatten
↓
Dense (128, ReLU)
↓
Dense (64, ReLU)
↓
Dense (10, Softmax)
Total Parameters:

109,386

🧮 Mathematical Formulation

Hidden layers use ReLU activation:

𝑅
𝑒
𝐿
𝑈
(
𝑥
)
=
𝑚
𝑎
𝑥
(
0
,
𝑥
)
ReLU(x)=max(0,x)

Output layer uses Softmax:

𝑃
(
𝑦
=
𝑖
)
=
𝑒
𝑧
𝑖
∑
𝑒
𝑧
𝑗
P(y=i)=
∑e
z
j
	​

e
z
i
	​

	​


Loss function:

Categorical Crossentropy:

𝐿
=
−
∑
𝑦
𝑖
log
⁡
(
𝑦
^
𝑖
)
L=−∑y
i
	​

log(
y
^
	​

i
	​

)

Optimizer:

Adam (Adaptive Moment Estimation)

📈 Model Performance
Metric	Value
Training Accuracy	~99%
Validation Accuracy	~97.4%
Total Parameters	109,386

The small gap between training and validation accuracy indicates good generalization with minimal overfitting.

📊 Evaluation Techniques

Training vs Validation Accuracy Tracking

Loss Monitoring

Random Prediction Visualization

Wrong Prediction Analysis

Confusion Matrix

📷 Sample Predictions

The model predicts digits along with confidence scores.

Correct predictions are displayed in green, incorrect in red for easy error analysis.

📂 Project Structure
Hand_written_digit_detection/
│
├── digit.csv
├── notebook.ipynb
├── requirements.txt
├── .gitignore
└── README.md
🚀 Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/your-username/Hand-written-digit-detection.git
cd Hand-written-digit-detection
2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate
3️⃣ Install Dependencies
pip install -r requirements.txt
▶ Run the Project

Open Jupyter Notebook:

jupyter notebook

Run all cells to:

Train the model

Evaluate performance

Visualize predictions

🧪 Future Improvements

Implement CNN architecture for higher accuracy (~99%+)

Add Dropout for regularization

Hyperparameter tuning

Deploy as a web application (Flask/FastAPI)

Convert to real-time digit recognition using OpenCV

Save and load trained model (.h5 / .keras format)

💡 Key Learnings

Deep learning workflow

Data normalization importance

One-hot encoding

Model generalization

Overfitting detection

Evaluation metrics interpretation

🛠 Tech Stack

Python

NumPy

Pandas

Matplotlib

Scikit-learn

TensorFlow / Keras