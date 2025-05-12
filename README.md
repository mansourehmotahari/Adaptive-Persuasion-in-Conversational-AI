# 🧠 Adaptive Persuasive Chatbot using LLMs, Sentiment & Personality Analysis

This repository provides the implementation of  
**“Adaptive Persuasion in Conversational AI: An LLM-Driven Framework for Dynamic Strategy Switching via Personality and Sentiment Analysis,”**  
accepted at **ICWR 2025**.

---

## 🔍 Project Overview

A personalized persuasive chatbot that dynamically adapts its strategy in multi‑turn conversations through:

1. **Big Five Personality Profiling** – users represented by a five-dimensional vector (O, C, E, A, N).  
2. **Real-Time Sentiment Analysis** – classification of user utterances (positive, neutral, negative).  
3. **Dynamic Strategy Switching** – selection among persuasive strategies (emotional, logical, credibility, informative, …) via a formula combining personality and sentiment signals; strategy weights updated with reinforcement-learning-inspired logic.

The system employs **Large Language Models** (e.g., LLaMA) augmented with **Retrieval-Augmented Generation (RAG)** for context-aware, coherent responses.

---

## 🛠️ Implementation Details

| Component       | Description                                               |
| --------------- | --------------------------------------------------------- |
| Notebook        | `Sentiment_Analysis,_BERT,_LLM,_Groq.ipynb`               |
| Sentiment Model | `twitter-roberta-base-sentiment`                          |
| Language Model  | `llama-3.1-8b-instant`                                    |
| Dataset         | PersuasionForGood                                         |
| Strategy Types  | Emotional · Logical · Credibility-based · Informative · … |

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/<username>/adaptive-persuasion-chatbot.git
cd adaptive-persuasion-chatbot
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Execute the notebook

```bash
jupyter notebook Sentiment_Analysis,_BERT,_LLM,_Groq.ipynb
```

Run cells sequentially:

1. Data preprocessing  
2. Sentiment & personality modeling  
3. Strategy selection & weight adaptation  
4. Response generation with the LLM  

---

## 📓 Notebook Breakdown

The notebook is organized into several key stages:

### 1. Install Dependencies

Installs packages including `langchain`, `langchain-groq`, `sentence-transformers`, `googletrans`, etc.

### 2. Load and Preprocess Data

Uses sample text and sentiment examples to verify data flow. Persuasion and personality content is optionally fetched using `gdown` or translation tools.

### 3. Sentiment Analysis

Includes:

- Loading multilingual BERT and RoBERTa models via HuggingFace.
- Using pipelines to analyze sample sentences with Persian or English inputs.

### 4. Personality and Prompt Construction

Processes messages and configures prompts to guide persuasive responses depending on user personality and context.

### 5. Language Model Integration (Groq API)

Defines helper function `get_chat_completion()` that sends prompts to Groq-hosted `llama-3.1-8b-instant`, using OpenAI-compatible API endpoints. Returns response content.

### 6. Strategy Simulation

Constructs simulated messages with tags like `[Logical]`, `[Emotional]`, etc., and generates responses using LLM for testing strategy effectiveness.

---

## 📊 Results

| Metric              | Static Strategy | Dynamic Strategy | Adaptive Strategy |
| ------------------- | --------------- | ---------------- | ----------------- |
| Dialogue Turns      | 9 ± 1.8         | 12.7 ± 2.4       | 14.5 ± 3.9        |
| Donation (USD)      | 0.5             | 17.5             | 20.0              |
| Empathy Score (1-5) | 1.5             | 3.2              | 3.2               |

Adaptive and dynamic variants significantly outperform the static baseline across all metrics.

---

## 📁 Project Structure

```
├── README.md
├── Copy_of_Sentiment_Analysis,_BERT,_LLM,_Groq.ipynb
├── paper/
│   └── ICWR2025_1263953.pdf
├── assets/                  # optional visualizations or samples
└── requirements.txt
```

---

## 📚 Citation

```
@inproceedings{motahari2025adaptive,
  title  = {Adaptive Persuasion in Conversational AI: An LLM-Driven Framework for Dynamic Strategy Switching via Personality and Sentiment Analysis},
  author = {Motahari Nezhad, Mansoureh and Avakh Kisomi, Maysam and Gholinezhad, Fatemeh},
  booktitle = {International Conference on Web Research (ICWR)},
  year   = {2025}
}
```

---

## 📜 License

Released under the Apache-2.0 license.

---

## 📬 Contact

- mansoureh_motahari@alumni.iust.ac.ir  / motahari.mansoureh@gmail.com
- sinaavakh@gmail.com  
- f.gholinezhad@gmail.com
