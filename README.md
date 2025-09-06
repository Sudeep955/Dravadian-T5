# 🌐 Dravidian-T5: A Neural Machine Translation Approach for Dravidian Languages  

Dravidian-T5 is a **multilingual Neural Machine Translation (NMT) model** fine-tuned for **low-resource Dravidian languages** (Kannada, Tamil, Telugu, Malayalam).  
It is built using a **pivot-based data augmentation framework** and a **compressed, language-specific version of mT5**.  

This project also introduces:  
- 📂 **DraPara**: A 100k+ high-quality parallel corpus  
- 🤖 **Dravidian-T5 Model**: A lightweight, efficient translation model for inclusive NLP  

---

## ✨ Highlights  
- 🔁 **Pivot-based augmentation** using English as an intermediary  
- 🔤 **Multilingual translation** across 4 Dravidian languages  
- 🧠 **Optimized T5 model** (~20% smaller than mT5, with 23% fewer FLOPs)  
- 📂 **Dataset & Model available** on Hugging Face  

---

## 📊 Dataset: DraPara  

- 📚 **Source**: Samanantar Kn–En Dataset  
- 🔁 Translated from **English → Tamil, Telugu, Malayalam** using **NLLB-200**  
- 🧹 Filtered with **BLEU > 0.5** and **Semantic Similarity > 0.8**  
- 📦 **Final size**: `107,057` high-quality sentence pairs  
- 📍 Hosted on Hugging Face: [DraPara Dataset](#) *(replace with link)*  

---

## 🤖 Model: Dravidian-T5  

- **Base Model**: `google/mt5-small`  
- **Vocabulary**: Reduced to top Dravidian language tokens  
- **Preprocessing**: Language-tagged sentences (e.g., `<kn> ... </kn>`)  
- **Training**: Joint multilingual fine-tuning on DraPara corpus  
- 🚀 Hosted at: [Dravidian-T5 Model](#) *(replace with link)*  

---

## 🧪 Evaluation  

| Language Pair       | BLEU  | Similarity |
|---------------------|-------|------------|
| Kannada ↔ Tamil     | 6.52  | 0.7203     |
| Kannada ↔ Telugu    | 6.75  | 0.7484     |
| Kannada ↔ Malayalam | 6.39  | 0.7168     |
| Tamil ↔ Telugu      | 5.98  | 0.7146     |

- 📊 **Average BLEU**: `0.69`  
- 🤝 **Average Similarity**: `0.7764` (on 1000 unseen sentences/language)  
- 🔬 Evaluation metrics: **Indic-SBERT** + **sentence-BLEU**  

---

## 💡 Example  

**Input (Kannada):**  
