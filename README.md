#  Next Word Prediction using LSTM & Streamlit

This project implements a **Next Word Prediction** model trained on *Hamlet* by William Shakespeare using **LSTM (Long Short-Term Memory)** networks.  
It also provides an **interactive Streamlit web app** to try out predictions in real time.

---

##  Features
- **Trains on Shakespeare's Hamlet** from the NLTK Gutenberg corpus.
- **Preprocessing pipeline** — tokenization, n-gram sequence creation, and padding.
- **Deep learning model** — built using TensorFlow Keras with:
  - Embedding Layer
  - Two LSTM layers
  - Dropout for regularization
  - Dense softmax output
- **Next Word Prediction** — given an input phrase, predicts the most probable next word.
- **Streamlit UI** — interactive interface for user input and predictions.
- **Early Stopping** — prevents overfitting during training.

---

##  Installation

### 1️ Clone the Repository
git clone https://github.com/HarshithaDevanga/LSTM-predict-the-next-word.git
cd LSTM-predict-the-next-word

### 2️ Create and Activate a Virtual Environment
python -m venv venv
source venv/bin/activate # Mac/Linux
venv\Scripts\activate # Windows

### 3️ Install Dependencies
pip install -r requirements.txt

---

## Project Structure
├── app.py # Streamlit app for prediction
├── experiments.ipynb # Notebook for model training
├── hamlet.txt # Dataset (Shakespeare's Hamlet)
├── tokenizer.pickle # Saved tokenizer
├── next_word_lstm.h5 # Trained LSTM model (if present)
├── requirements.txt # Python dependencies
└── README.md # Project documentation

---

##  Usage

###  Training the Model
Open `experiments.ipynb` in Jupyter Notebook or VS Code and run all cells.  
This will:
- Download and preprocess the Hamlet text.
- Train the LSTM model with EarlyStopping.
- Save:
  - The trained model file (`.h5` or `.keras`)
  - The tokenizer (`tokenizer.pickle`)

###  Running the Streamlit App
After training (or if you already have the saved model and tokenizer files):
streamlit run app.py
Go to the URL displayed in the terminal (usually `http://localhost:8501`).

---

##  Model Details
- **Embedding Layer**: Converts word indices into dense vectors (size=100).
- **LSTM Layers**: Two layers to capture sequential dependencies.
- **Dropout**: Reduces overfitting by randomly setting inputs to zero.
- **Dense Output Layer**: Softmax over the entire vocabulary for prediction.

---

##  Example
**Input:**
To be or not to
**Predicted Next Word:**

---

##  Dataset
We use **NLTK's Gutenberg corpus**:
- File: `shakespeare-hamlet.txt`
- Preprocessed: Lowercased, tokenized, converted to integer sequences.

---

##  Future Improvements
- Train on larger, more diverse corpora for general usage.
- Implement beam search for better next-word prediction.
- Deploy as a public web app using Streamlit Cloud, Hugging Face Spaces, or Heroku.
- Extend to sentence completion or text generation.

---

##  License
This project is licensed under the MIT License - see the LICENSE file for details.

---

##  Author
- **DeepakAthreshR** — Software Engineer Intern
- **HarshithaDevanga** —  AI Software Engineer Intern



