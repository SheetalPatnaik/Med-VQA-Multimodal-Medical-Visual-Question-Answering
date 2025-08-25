# 🏥 Med-VQA — Multimodal Medical Visual Question Answering

Hi, I’m **Sheetal Patnaik** 👋  

This repository contains my end-to-end **Medical Visual Question Answering (Med-VQA)** system.  
I designed this project to blend **vision-language models (VLMs)** with **Retrieval-Augmented Generation (RAG)** and **advanced prompting strategies (Chain-of-Thought, Tree-of-Thought, Few-shot prompting)**.  

My goal: build a Med-VQA system that is **accurate, explainable, and clinically meaningful**.  

---

## 🔑 Key Contributions
- **Multimodal RAG Pipeline** → integrates visual embeddings (CLIP) and biomedical text retrieval (PubMedQA, SLAKE) using FAISS.  
- **Prompting Strategies** → Zero-shot, Few-shot, **CoT**, **ToT**. CoT/ToT achieved **77% recall**, outperforming fine-tuned baselines.  
- **LoRA Fine-Tuning** → Adapted **LLaVA-Med (7B)** using efficient fine-tuning (r=4, α=16, dropout=0.05). Baseline accuracy ~54%.  
- **Answer Validation Loop** → enforced structured outputs (A/B/C/D) and re-asked when uncertain responses appeared.  
- **Explainability with MedCoT** → introduced structured reasoning traces for more transparent clinical AI.  

---

## 🧪 Datasets Used
- **PMC-VQA** → 227k QA pairs from 149k medical images (X-ray, MRI, CT, pathology).  
- **SLAKE** → 642 medical images, 14k QA pairs (used for retrieval).  
- **PubMedQA** → biomedical literature dataset with yes/no/maybe answers.  
- Benchmarks: **VQA-RAD, PathVQA, Med-VQA 2019, ImageCLEF-VQA**.  

> ⚠️ Datasets are not included in this repo. Please download from their official sources.

---

## ⚙️ Tech Stack
- **Models**: LLaVA-Med, GPT-4 (prompting), CLIP ViT-B/32, PMC-CLIP  
- **Libraries**: PyTorch, Transformers, Sentence-Transformers, FAISS, OpenAI/CLIP  
- **Paradigms**: RAG, Chain-of-Thought, Tree-of-Thought, Few-shot, LoRA Fine-Tuning  

---


👉 **Prompting + Retrieval > Fine-Tuning** for generalization and interpretability.

---

## 📂 Repository Contents
- **`/notebooks`** → Implementation notebooks (RAG pipeline, prompting, LoRA fine-tuning).  
- **`/reports`** → Final report & proposal (detailed methodology, evaluation, and limitations).  
- **`/slides`** → Presentation deck.  
- **`/data`** → Placeholder for dataset instructions (no raw data).  

---

## ▶️ Quickstart
```bash
# 1. create environment
python -m venv .venv
source .venv/bin/activate

# 2. install dependencies
pip install -r requirements.txt

# 3. run notebooks
jupyter lab
