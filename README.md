# Portuguese Misogyny Detection: A BERT Model Benchmark & Streamlit Interface

This repository features a robust Natural Language Processing (NLP) pipeline dedicated to identifying and classifying misogynistic speech in Portuguese text. Instead of relying on a single architecture, this project evaluates and benchmarks four advanced BERT-based models to discover the most precise and reliable solution for toxic content moderation.

---

## 🔬 Models Evaluated & Benchmark

We fine-tuned and compared the performance of 4 distinct pre-trained deep learning architectures using Hugging Face and PyTorch:

*   **BERTimbau Large** (Top Performer 🏆)
*   **BertoMelo Large**
*   **XLM-RoBERTa Base**
*   **BERT Large**

---

## 📊 Evaluation & Metrics

To ensure a rigorous and reliable evaluation—especially considering potential class imbalances often found in hate speech datasets—the models were evaluated using the following criteria:

1.  **F1-Score:** Used as the primary optimization and comparison metric to perfectly balance *Precision* and *Recall*. This ensures the model effectively catches misogyny without over-classifying neutral texts.
2.  **Confusion Matrix:** Thoroughly analyzed during the validation phase to minimize both False Positives (preventing censorship of benign content) and False Negatives (preventing hate speech from passing undetected).

**BERTimbau Large** achieved the best overall F1-Score, demonstrating a superior capability in understanding the slangs, subtle nuances, and cultural context of the Portuguese language.

---

## 🖥️ Streamlit Web Interface

The best-performing model (**BERTimbau**) was integrated into an interactive web application built with **Streamlit**. This allows users and content moderators to test the model in real-time.

### Key Features:
*   **Real-time Analysis:** Input any text, sentence, or social media comment.
*   **Instant Classification:** Predicts whether the text contains misogynistic speech.
*   **Confidence Score Visualization:** Interactive visual feedback showing how confident the model is about its prediction.

---

## 🛠️ Tech Stack

*   **Language:** Python
*   **NLP & Deep Learning:** Hugging Face (Transformers), PyTorch
*   **Web Application:** Streamlit
*   **Metrics & Evaluation:** Scikit-learn
*   **Infrastructure:** Google Colab / NVIDIA GPU T4 (Fine-tuning phase)

---

## 🚀 How to Run the Project Locally

### 1. Clone the Repository
```bash
git clone [https://github.com/AdrielleMarques/nlp-misogyny-detector-pt.git](https://github.com/AdrielleMarques/nlp-misogyny-detector-pt.git)
cd nlp-misogyny-detector-pt

2. Install Dependencies
Make sure you have Python installed, then run:
pip install -r requirements.txt

3. Run the Streamlit App
streamlit run app.py

📂 Project Structure (Suggested)
├── app.py                
├── requirements.txt      
├── notebooks/            
├── presentation/         
└── README.md             
