# Emotion Detection in Text

This project explores emotion classification from textual data using both deep learning (CNN-LSTM) and large language models (LLMs). The objective is to evaluate the effectiveness of different models in detecting human emotions across various datasets, and to examine the potential of lightweight LLMs for local inference.

## 📌 Project Highlights

- **Replicated a CNN-LSTM model** from the paper [Deep Learning-Based Emotion Recognition Using CNN-LSTM](https://www.mdpi.com/2076-3417/10/18/6444)
- **Evaluated large language models (LLMs)** including encoder-only (e.g., `all-MiniLM`, `mpnet`, `gtr-t5`) and decoder-only models (e.g., `TinyLLaMA`, `Mistral`)
- **Compared performance across models and emotions**
- **Focused on clean and reproducible experiments** using structured notebooks and code

## 🔍 Emotion Dataset

Based on a real-world text emotion dataset with the following classes:

- `joy`, `sadness`, `anger`, `fear`, `disgust`, `surprise`, `shame`, `neutral`

### Sample Entry

| Emotion | Text | Cleaned Text |
|--------|------|---------------|
| Joy | "Looking forward to tomorrow!" | "looking forward tomorrow" |

## 🧠 Models Evaluated

| Model | Type | Size |
|-------|------|------|
| CNN-LSTM | Deep Learning | ~0.5M |
| all-MiniLM-L12-v2 | Encoder-only | 66M |
| all-MPNet-Base-V2 | Encoder-only | 109M |
| GTR-T5-XL | Encoder-only | 3.7B |
| TinyLLaMA | Decoder-only | 1.1B |
| Mistral | Decoder-only | 7B |

## 📊 Results Summary

- CNN-LSTM achieved **high accuracy**, especially on `joy`, `sadness`, and `fear`, with fast local inference.
- Lightweight LLMs like `TinyLLaMA` and `Mistral` underperformed compared to DL methods.
- Encoder-only models showed **moderate accuracy**, especially on `joy` and `sadness`.
- Larger LLMs demonstrate potential but are heavily constrained by size and computational resources.

## 🛠️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/YitongGu/Emotion-Detection-in-Text.git
   cd Emotion-Detection-in-Text
