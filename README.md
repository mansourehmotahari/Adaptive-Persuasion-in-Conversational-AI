# 🧠 Adaptive Persuasive Chatbot using LLMs, Sentiment & Personality Analysis

This repository provides the implementation of  
**“Adaptive Persuasion in Conversational AI: An LLM-Driven Framework for Dynamic Strategy Switching via Personality and Sentiment Analysis,”**  
accepted at **ICWR 2025**.

---

## 🔍 Project Overview

A personalized persuasive chatbot that dynamically adapts its strategy in multi-turn conversations through:

1. **Big Five Personality Profiling** – users represented by a five-dimensional vector (O, C, E, A, N).  
2. **Real-Time Sentiment Analysis** – classification of user utterances (positive, neutral, negative).  
3. **Dynamic Strategy Switching** – selection among persuasive strategies (emotional, logical, credibility, informative, …) via a formula combining personality and sentiment signals; strategy weights updated with reinforcement-learning-inspired logic.

The system employs **Large Language Models** (e.g., LLaMA) augmented with **Retrieval-Augmented Generation (RAG)** for context-aware, coherent responses.

---

## 🛠️ Implementation Details

| Component        | Description                                                    |
|------------------|----------------------------------------------------------------|
| Notebook         | `Copy_of_Sentiment_Analysis,_BERT,_LLM,_Groq.ipynb`            |
| Sentiment Model  | `twitter-roberta-base-sentiment`                               |
| Language Model   | `llama-3.1-8b-instant`                                         |
| Dataset          | PersuasionForGood                                              |
| Strategy Types   | Emotional · Logical · Credibility-based · Informative · …      |

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/<username>/adaptive-persuasion-chatbot.git
cd adaptive-persuasion-chatbot
