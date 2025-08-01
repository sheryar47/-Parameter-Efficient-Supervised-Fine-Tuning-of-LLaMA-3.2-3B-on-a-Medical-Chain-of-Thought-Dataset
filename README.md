# 📝 AI Text Summarization using Transformers (BART)

Automatically generate concise and meaningful summaries from long English articles using state-of-the-art transformer models!

---

## 🚀 Project Overview

With the ever-growing volume of digital content, it's challenging to keep up with lengthy news, reports, and articles.  
This project leverages a powerful **pretrained BART transformer model** to summarize long texts into short, human-like summaries, helping users save time and focus on key insights.

---

## 🔥 Features

- 📚 Summarizes any English article or paragraph in seconds
- 🤗 Uses [Hugging Face](https://huggingface.co/) transformers (BART model)
- 🖥️ No GPU required—runs on standard laptops or desktops
- 🗣️ Interactive script: just paste your text, and get an instant summary!
- 🛠️ Easily customizable for length or style of summaries

---

## 💻 Demo

```python
# Import libraries
from transformers import pipeline

# Load pretrained summarization pipeline (BART)
summarizer = pipeline("summarization", model="facebook/bart-large-cnn")

# User input
text = input("Paste your article here:\n")

# Summarize
summary = summarizer(text, max_length=130, min_length=30, do_sample=False)
print("\n--Summary--\n", summary[0]['summary_text'])
