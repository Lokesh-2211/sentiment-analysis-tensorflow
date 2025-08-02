# 🧠 Sentiment Analysis Using TensorFlow

Welcome! This is a beginner-friendly machine learning project where I built a sentiment analysis model using TensorFlow. The model can read financial news or sentences and figure out whether the sentiment is **positive**, **negative**, or **neutral**.

I followed this project to practice **text classification**, **deep learning**, and **model tuning** — and learned a lot along the way!

---

## 🌟 What This Project Does

This project takes a bunch of financial-related sentences (like those found in news articles or social media) and teaches a neural network to guess the **sentiment** behind them.

Example:
"The company reported excellent quarterly results." → Positive
"The economy is under pressure from inflation." → Negative
"Markets remained stable throughout the day." → Neutral


---

## 🧰 Tools & Technologies Used

- **Python** 🐍  
- **TensorFlow / Keras** for building the deep learning model  
- **Keras Tuner** for finding the best model parameters  
- **Pandas / NumPy** for data handling  
- **Matplotlib** for visualizing results  
- **Colab** for running everything in the cloud (no setup!)

---

## 🗂️ What's Inside This Repo

| File | What it is |
|------|------------|
| `Main.ipynb` | My full notebook: data loading, preprocessing, model training, and tuning |
| `Sentences_75Agree_sample.txt` | The dataset I used (a list of labeled financial sentences) |
| `finalModel.zip` | A compressed version of my trained model (contains `finalModel.h5`) |
| `requirements.txt` | Python libraries used (you can install them if running locally) |
| `README.md` | You're reading it! 🎉 |

---

## 🔍 Step-by-Step: What I Did

### 1️⃣ Loaded and Explored the Dataset  
I started with a `.txt` file containing financial sentences and their sentiment labels (0 = negative, 1 = neutral, 2 = positive). I looked at the data, checked the distribution of labels, and did basic cleaning.

### 2️⃣ Preprocessed the Text  
- Cleaned the text (removed punctuation, lowercased, etc.)  
- Tokenized the words  
- Converted them into numbers using **TF-IDF vectorization**

### 3️⃣ Built a Basic Neural Network  
Using Keras, I built a model with:
- One or two `Dense` layers
- `Dropout` to prevent overfitting
- `Softmax` output layer for the 3 sentiment classes

### 4️⃣ Tuned the Model with Keras Tuner  
I used Keras Tuner to try different:
- Number of units in the layers
- Activation functions (`relu` or `tanh`)
- Dropout rates

📈 Best validation accuracy: **~85.95%**

### 5️⃣ Saved the Best Model  
Once the model was trained, I saved it as `finalModel.h5` and zipped it as `finalModel.zip` to make it easier to upload.

---

## ▶️ How to Use This Project

You can run the notebook on **Google Colab** or locally if you prefer.

### 💻 Option 1: Run in Colab  
1. Open `Main.ipynb` in Google Colab  
2. Upload the dataset and run each cell step-by-step  
3. The notebook will:
   - Load the data
   - Preprocess it
   - Train and tune the model
   - Save the final model

### 💻 Option 2: Load My Pretrained Model  
After downloading and unzipping `finalModel.zip`, you can load the model like this:

```python
from tensorflow import keras
model = keras.models.load_model('finalModel.h5')
