# 📰 News Topic Classifier Using DistilBERT

## Project Overview
This project fine-tunes a **DistilBERT** transformer model to automatically classify news headlines into 4 categories. The model achieves **94.62% accuracy** on the AG News dataset.

### Categories
| # | Category | Emoji | Example Headline |
|---|----------|-------|------------------|
| 0 | World | 🌍 | "US and China agree to new trade deal" |
| 1 | Sports | ⚽ | "Manchester United wins Premier League title" |
| 2 | Business | 💼 | "Tesla stock surges after record earnings" |
| 3 | Sci/Tech | 🔬 | "NASA discovers new exoplanet in habitable zone" |

## 📊 Model Performance

### Overall Metrics
- **Accuracy:** 94.62%
- **F1-Score:** 0.9462
- **Test Loss:** 0.1708
- **Training Time:** 23.5 minutes on Tesla T4 GPU

### Per-Category Performance
| Category | Precision | Recall | F1-Score |
|----------|-----------|--------|----------|
| World | 0.96 | 0.95 | 0.96 |
| Sports | 0.99 | 0.99 | 0.99 |
| Business | 0.93 | 0.91 | 0.92 |
| Sci/Tech | 0.91 | 0.93 | 0.92 |

### Sample Predictions
| Headline | Prediction | Confidence |
|----------|------------|------------|
| "Apple announces new iPhone with advanced AI features" | Sci/Tech | 96.74% |
| "Manchester United wins Premier League title" | World | 86.22% |
| "Global stock markets rally after Fed announcement" | Business | 99.48% |
| "Scientists discover breakthrough in quantum computing" | Sci/Tech | 93.97% |

## 🛠️ Technical Details

### Model Architecture
- **Base Model:** DistilBERT-base-uncased
- **Type:** Transformer (6 layers)
- **Total Parameters:** 66,956,548
- **Model Size:** 255 MB

### Training Configuration
- **Dataset:** AG News (120,000 training, 7,600 test)
- **Batch Size:** 32
- **Epochs:** 2
- **Learning Rate:** 2e-5
- **Optimizer:** AdamW
- **Mixed Precision:** FP16

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Upload `News_Classifier_BERT.ipynb` to Google Colab
2. Set runtime type to **GPU (T4)**
3. Run all cells sequentially
4. Get your public Gradio link at the end

### Option 2: Local Machine
```bash
# Install dependencies
pip install torch transformers datasets scikit-learn gradio

# Run the notebook
jupyter notebook News_Classifier_BERT.ipynb

## 📄 License
MIT
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/effc74cf-2556-4833-a363-aa409dd51e3f" />

🌐 Live Demo
The model is deployed with Gradio. Click the link below to test it live:

🔗 https://af0c5e7583bc169b3.gradio.live

Note: This link expires in 1 week. For permanent hosting, deploy to Hugging Face Spaces.
💡 What I Learned
Fine-tuning transformer models (DistilBERT/BERT) for text classification

Transfer learning and model adaptation for downstream tasks

Tokenization and data preprocessing for NLP

Model evaluation using accuracy and F1-score

Deploying ML models with Gradio for interactive web apps

📝 Author
Zaryab Ahmad

📅 Date
April 2026


