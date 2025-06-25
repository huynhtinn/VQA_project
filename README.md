
# 🧠 Generative VQA: End-to-End Visual Question Answering System

## 🌟 Overview

This repository presents a full **end-to-end Visual Question Answering (VQA)** pipeline, from dataset generation using **generative AI** to training a **custom deep learning model** that can answer natural-language questions about images of animals.

---

## ✨ Core Features

- 🤖 **Automated Dataset Generation** using BLIP + Gemini APIs  
- 🖼️ **Image Captioning** with BLIP  
- 📄 **Question-Answer Pair Generation** with Gemini API  
- 🧠 **Custom VQA Model**: CNN + LSTM + Attention + LSTM Decoder  
- 📈 **Training & Evaluation** with visual outputs and loss tracking  
- ⚡ **Colab-Ready**: Easy to run with GPU support

---

## 🔄 Project Pipeline

### Stage 1: Automated Dataset Creation

```mermaid
graph LR
    A[Animal Image] --> B[BLIP Captioning]
    B --> C[Caption Text]
    C --> D[Gemini Q&A Generation]
    D --> E[Q&A JSON Dataset]
````

* **BLIP**: Generates captions for each image
* **Gemini API**: Uses captions to create question-answer pairs

---

### Stage 2: Model Training & Evaluation

* 📥 **Input**: (Image, Question) → 🧠 VQA Model → 📤 Answer
* 🔍 Model Architecture:

  * **CNN**: Extract visual features
  * **LSTM (Q)**: Encode question
  * **Attention**: Align question with image features
  * **LSTM (Answer)**: Generate output tokens
* 🧪 **Evaluation**: Visualize predictions & training loss

---

## 🚀 How to Run

1. **Open the notebook** in Colab
2. **Enable GPU**: Runtime → Change Runtime Type → GPU
3. **Mount Google Drive** for persistent storage
4. **Set paths** inside the notebook
5. **Run Cells**:

   * 🔸 Captioning (`generate_caption()`)
   * 🔸 Q\&A Generation (`get_gemini_qna_json()`)
   * 🔸 Model Training (`train_vqa()`)

> ⚠️ You need a Gemini API Key:

```python
os.environ['GOOGLE_API_KEY'] = 'YOUR_API_KEY_HERE'
```

---

## 🧪 Live Demo

Want to try it out? 👉 Click below to test the VQA model directly in your browser:

<p align="center">
  <a href="https://huggingface.co/spaces/Tin113/vqa_project">
    <img src="https://img.shields.io/badge/HuggingFace-%F0%9F%A4%97-yellow">
  </a>
</p>

Upload an animal image, ask a question, and get an answer from our VQA model — no installation required!


🧑‍🏫 This project was developed for the **Deep Learning course** at **Ton Duc Thang University**.

