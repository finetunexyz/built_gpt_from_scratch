# NanoGPT: A Minimal Transformer Language Model

NanoGPT is a simplified, educational implementation of a Transformer-based language model inspired by the *Attention Is All You Need* paper (2017) and GPT-style architectures.  
It trains a character-level language model on the **Tiny Shakespeare corpus (~1MB)** to highlight the core mechanisms behind models like GPT and ChatGPT.

---

## 📖 Overview

- **Task:** Next-character prediction (language modeling).  
- **Approach:** Autoregressive Transformer (decoder-only) with causal masking.  
- **Dataset:** Tiny Shakespeare, tokenized at the character level (~65 tokens).  
- **Output:** Generates Shakespeare-like text via probabilistic sampling.

---

## ⚙️ Key Components

### Transformer Foundations
- **Self-Attention:** Each token attends to past tokens (causal masking).  
- **Multi-Head Attention:** Parallel heads learn diverse token relationships.  
- **Positional Embeddings:** Encodes order since attention is permutation-invariant.  
- **Feed-Forward Layers + Residual Connections:** Enhance expressiveness and stability.  
- **Layer Norm & Dropout:** Stabilize training and reduce overfitting.  

### Data Handling
- **Train/Val Split:** 90% / 10%.  
- **Block Sampling:** Trains on fixed-length random chunks of text.  
- **Baseline:** Starts with a simple **bigram model** to illustrate need for context.

### Training
- **Loss:** Cross-entropy.  
- **Optimizer:** Adam.  
- **Autoregressive Generation:** Sequential token prediction with sampling.  

---

## 🚀 Scaling & Performance
- Increasing model size (embedding dims, layers, heads, context) → lower validation loss & more coherent text.  
- Even small models generate creative Shakespearean-style text, though often nonsensical.  

---

## 🔗 Relation to GPT
NanoGPT mirrors GPT pretraining:
- **Same core mechanism:** next-token prediction.  
- **Simplified:** Character-level tokens, smaller dataset, ~200 lines of code.  
- **Excludes:** Fine-tuning, alignment, and RLHF (used in ChatGPT).  

---

## 🎯 Educational Value
This project **distills Transformers into minimal, readable code**, making it easier to:
- Understand self-attention, embeddings, and training dynamics.  
- Experiment with scaling, tokenizers, and datasets.  
- Build intuition for how large models like GPT are trained.  

---

## 📂 Resources
- Paper: [Attention Is All You Need (2017)](https://arxiv.org/abs/1706.03762)  
- Dataset: [Tiny Shakespeare](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)  

---

### 📝 License
MIT License
