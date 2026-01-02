# LLMs Prompt Engineering & RAG for Text Classification

This project explores how different **LLM prompting techniques** perform on a **text classification task**, and how **Retrieval-Augmented Generation (RAG)** can be used to **improve lower-performing prompt methods without fine-tuning**.

The core mission of this project is:

> **Identify prompt techniques with lower accuracy and systematically improve them using RAG-based approaches.**

---

## 🎯 Project Objectives

- Evaluate multiple **prompt engineering techniques** for classification
- Identify **weaker-performing prompts**
- Improve their performance using:
  - Self-Consistency
  - CARP prompting
  - Retrieval-Augmented Generation (RAG)
  - RAG + Few-Shot prompting
- Compare results quantitatively

---

## 🧠 Prompting & Reasoning Techniques

The following techniques were implemented and evaluated:

### 1. Zero-Shot Prompting
- No examples provided
- Relies purely on model prior knowledge

### 2. Few-Shot Prompting
- Uses a small number of labeled examples
- Helps guide decision boundaries

### 3. Chain-of-Thought (CoT)
- Encourages step-by-step reasoning before prediction

### 4. CARP (Context-Aware Reasoning Prompting)
- Injects task rules and label constraints
- Reduces ambiguous reasoning

### 5. Self-Consistency
- Generates multiple reasoning paths
- Uses majority voting for the final label
- Improves robustness and stability

---

## 📚 Retrieval-Augmented Generation (RAG)

RAG was introduced to:
- Retrieve relevant samples from the dataset
- Inject factual and contextual grounding into prompts
- Reduce hallucinations and weak generalization

Two variants were tested:
- **RAG only**
- **RAG + Few-Shot**

---

## 📊 Experimental Results

| Technique | Accuracy (%) |
|---------|--------------|
| Zero-Shot | 95.7 |
| Few-Shot | 91.3 |
| Chain-of-Thought (CoT) | 91.9 |
| CARP | 91.8 |
| **Self-Consistency** | **98.8** |
| RAG (Only) | 96.0 |
| **RAG + Few-Shot** | **98.0** |

---

## 🔍 Key Findings

- **Few-Shot, CoT, and CARP** had noticeably lower accuracy (~91%)
- **RAG significantly improved performance** over these weaker prompts
- **RAG + Few-Shot** achieved near state-of-the-art results without model fine-tuning
- **Self-Consistency** delivered the highest accuracy overall by stabilizing reasoning paths

---

## ✅ Conclusion

This project demonstrates that:

- Prompt engineering alone is often insufficient
- **RAG is a powerful tool to rescue low-performing prompts**
- Combining **retrieval + examples + reasoning control** can rival advanced fine-tuning
- Significant gains are achievable **without changing the model**

---

## 🚀 Future Work

- Automatic retrieval ranking
- Adaptive example selection
- Multi-label classification
- Cost vs accuracy analysis

---

⭐ If you find this project useful, feel free to star the repository!
