# Model-finetune-for-Sinhala-songs
🎶 This is the repository for finetuning different models with different datasets to give knowledge about Sinhala songs in different eras.

# 📌 First Fine-Tuning Attempt (Baseline Experiment)

This repository contains my first experimental attempt at fine-tuning a Large Language Model (LLM) for Sinhala song lyrics and metaphor understanding using parameter-efficient fine-tuning (LoRA). The goal of this attempt was to learn and implement the end-to-end fine-tuning workflow, including dataset preparation, model loading, quantization, training, and inference.

---

## 🧠 Model Used

- **Base Model:** `unsloth/Meta-Llama-3.1-8B-Instruct-bnb-4bit`
- **Model Type:** Instruction-tuned LLaMA 3.1
- **Quantization:** 4-bit (bnb)
- **Framework:** Unsloth
- **Fine-Tuning Method:** LoRA (Low-Rank Adaptation)

### Why this model?

- Efficient fine-tuning on limited GPU resources
- Faster training and lower memory usage
- Suitable for experimentation and learning LLM fine-tuning workflows

---

## 📚 Dataset Used

- **Dataset Name:** `pasinduudawatta/sinhala-songs-and-metaphors`
- **Source:** kaggle Datasets
- **Domain:** 
  - Sinhala song lyrics
  - Metaphorical expressions
  - Cultural and poetic language

### Dataset Purpose

To adapt the model toward:
- Understanding Sinhala lyrics
- Generating or interpreting metaphorical language
- Learning cultural linguistic patterns

---

## ⚙️ Training Setup

- **Fine-Tuning Type:** Supervised Fine-Tuning (SFT)
- **LoRA Configuration:**
  - LoRA applied on attention layers
  - Reduced trainable parameters
- **Precision:** 4-bit quantized weights
- **Environment:** Google Colab
- **Libraries:**
  - `unsloth`
  - `transformers`
  - `trl`
  - `datasets`

---

## 📊 Results & Observations

### ✅ Successfully:

- Loaded and quantized the model
- Applied LoRA adapters
- Fine-tuned on Sinhala text data
- Saved and tested the trained model

### ⚠️ Limitations observed:

- Output quality was not consistently accurate
- Weak understanding of deep metaphors
- Some hallucinations and irrelevant responses
- Dataset size and structure likely insufficient for the task
- Possible mismatch between instruction format and dataset style

> **Note:** This attempt is considered a baseline experiment, not a final production-ready model.

---

## 🧪 Key Learnings from First Attempt

### Importance of:

- Dataset quality and diversity
- Proper instruction formatting
- Domain alignment with base model

### Technical Insights:

- LoRA + 4-bit quantization works well for rapid experimentation
- Sinhala language modeling requires:
  - Larger and cleaner datasets
  - Better prompt-response alignment
  - Possibly multilingual or language-specialized base models

---

## 🚀 Next Steps (Planned Improvements)

- [ ] Try different base models (multilingual / Sinhala-friendly)
- [ ] Improve dataset:
  - Better instruction-response pairs
  - Cleaner annotations
  - Larger sample size
- [ ] Experiment with:
  - Different LoRA ranks
  - Training hyperparameters
  - Prompt templates
- [ ] Compare results across multiple fine-tuning attempts

---

## 🧾 Project Status

🟡 **Work in Progress**

This repository documents my learning journey in LLM fine-tuning, and future experiments will be added as separate attempts with improved methodologies.
