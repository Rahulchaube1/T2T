# 🧠 T2T — Text-to-Text AI Transformation Engine

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20Transformers-FFD21E?style=flat-square)](https://huggingface.co)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()

> A lightweight, modular **Text-to-Text** transformation framework built on top of transformer architectures. T2T enables flexible NLP pipelines for summarization, translation, paraphrase generation, and style transfer — all unified under a single inference API.

---

## 🚀 Overview

T2T (Text-to-Text) is designed around the T5/BART paradigm where every NLP task is framed as a sequence-to-sequence problem. Whether you want to summarize an article, translate between languages, rewrite text in a different style, or answer questions from context — T2T handles it through one unified interface.

---

## ✨ Features

| Feature | Description |
|:---|:---|
| 📝 **Summarization** | Condense long documents into concise summaries |
| 🌍 **Translation** | Multi-language text translation via seq2seq models |
| ✏️ **Paraphrase Generation** | Rewrite text while preserving semantic meaning |
| 🎨 **Style Transfer** | Transform tone, formality, or writing style |
| ❓ **Question Answering** | Extractive and generative QA from context |
| 🔌 **Pluggable Backends** | Swap between HuggingFace, OpenAI, or custom models |
| ⚡ **Batch Inference** | Efficient batch processing for large-scale text jobs |

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **PyTorch** — model training and inference
- **HuggingFace Transformers** — pretrained T5, BART, mT5 models
- **FastAPI** — REST API for serving predictions
- **Docker** — containerized deployment

---

## 📁 Project Structure

```
T2T/
├── models/          # Model wrappers and loaders
├── pipelines/       # Task-specific transformation pipelines
├── api/             # FastAPI server
├── utils/           # Preprocessing, tokenization helpers
├── configs/         # Model and task configuration files
├── examples/        # Usage examples and notebooks
└── README.md
```

---

## ⚡ Quick Start

```python
from t2t import T2TPipeline

# Summarization
pipeline = T2TPipeline(task="summarize", model="t5-base")
result = pipeline.run("Your long article text here...")
print(result.output)

# Translation
pipeline = T2TPipeline(task="translate", model="Helsinki-NLP/opus-mt-en-ne")
result = pipeline.run("Hello, how are you?")
print(result.output)  # Translated to Nepali
```

---

## 🤝 Contributing

PRs welcome! Please open an issue first to discuss major changes.

---

## 📄 License

MIT License © [Rahul Chaube](https://github.com/Rahulchaube1)

---

*Part of the [Artistic Impression](https://www.artisticimpression.org/) AI Research ecosystem.*
