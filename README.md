This project fine-tunes a large language model (LLM) on a **custom domain corpus** collected from websites using modern NLP tools.

## Project Highlights
- Uses **LoRA (Low-Rank Adaptation)** for memory-efficient LLM fine-tuning
- Scrapes and preprocesses structured documents with **LangChain + BeautifulSoup**
- Splits long documents using **RecursiveCharacterTextSplitter**
- Fine-tunes using Hugging Face's **SFTTrainer**

---

## Notebooks
- `dataset.ipynb`: Scrapes a domain and prepares text chunks for training
- `tuning.ipynb`: Fine-tunes a causal LLM using QLoRA on the cleaned dataset

---

## Tech Stack
- Python, Jupyter
- Hugging Face Transformers, TRL
- PEFT (QLoRA), LangChain, BeautifulSoup

---

## ⚠️ Known Limitations

While this project successfully demonstrates domain-specific fine-tuning using LoRA, there are some limitations:

- **Data Quality**: The scraped text, while relevant, contained some noise, formatting inconsistencies, and redundancies that may have impacted final model accuracy.
- **Training Size**: The dataset was relatively small for robust LLM adaptation, limiting generalization.
- **Evaluation**: Formal evaluation metrics (e.g., perplexity or BLEU scores) were not used to benchmark the tuned model.

These limitations are common in real-world NLP workflows and will be addressed in future iterations with improved data cleaning, larger corpora, and better evaluation pipelines.

---

## Usage

```bash
# Load and prepare data
Run dataset.ipynb

# Fine-tune the model
Run tuning.ipynb
