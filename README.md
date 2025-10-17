# 🧠 Duplicate Question Pair Detection App  

A **Streamlit web application** that detects whether two given questions are semantically similar (i.e., duplicates).  
The model is trained using advanced **NLP features**, including Bag-of-Words, token similarity, fuzzy matching, and length-based metrics.

---

## 🚀 Features  

- 🧹 Text preprocessing with stopword removal, decontraction, and special character handling  
- 🔤 Feature engineering: token, length, and fuzzy-based similarity features  
- 📊 Bag-of-Words representation for both questions  
- 🤖 Machine learning model (pre-trained) to classify *Duplicate* or *Not Duplicate*  
- 💻 Simple Streamlit interface for quick testing  

---

## 🗂️ Project Structure  

```
├── app.py                         # Streamlit app file  
├── helper.py                      # Helper functions for preprocessing & feature extraction  
├── bow-with-preprocessing-and-advanced-features.ipynb  # Notebook for training and feature generation  
├── model.pkl                      # Trained ML model  
├── cv.pkl                         # CountVectorizer pickle file  
└── requirements.txt               # Dependencies
```

---

## 🧰 Tech Stack  

- **Python 3.9+**  
- **Streamlit** for the web app interface  
- **scikit-learn** for ML model  
- **NLTK**, **TheFuzz**, **BeautifulSoup**, and **distance** for text processing  
- **NumPy & Pickle** for data handling and model loading  

---

## ⚙️ Installation  

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/Duplicate-Question-Pair-Detection.git
   cd Duplicate-Question-Pair-Detection
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate        # On Linux/Mac
   venv\Scripts\activate           # On Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Add the model files**
   - Ensure `model.pkl` and `cv.pkl` are present in the root directory.

---

## ▶️ Run the App  

```bash
streamlit run app.py
```

Then open your browser at **http://localhost:8501**  

---

## 🧪 How It Works  

1. Enter **two questions** in the text fields.  
2. The app converts them into feature vectors using:  
   - Token overlap  
   - Fuzzy ratios  
   - Length & structure similarity  
   - Bag-of-Words features  
3. The pre-trained model predicts whether they are *Duplicate* or *Not Duplicate*.  

---

## 🌐 Deployment  

To deploy on **Render**, **Streamlit Cloud**, or **Railway**, include a `setup.sh` and `requirements.txt` file.  
Example `setup.sh`:
```bash
mkdir -p ~/.streamlit/

echo "\
[server]\n\
port = $PORT\n\
enableCORS = false\n\
headless = true\n\
\n\
" > ~/.streamlit/config.toml
```

---

## 📘 Example  

**Input:**  
```
Question 1: What is the idea behind democracy?  
Question 2: What is the core idea behind democracy?
```
**Output:**  
```
Duplicate
```

---

## 🧑‍💻 Author  

**Ashutosh Shukla**  
🎓 B.Tech Student at IIIT Raichur  
💡 Passionate about NLP, Machine Learning, and AI-powered Applications  
