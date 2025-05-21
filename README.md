# RAG：Retrieval-Augmented Generation 實作與應用

本專案為一套基於 LangChain 框架所實作的論文檢索問答系統，結合語意切割、向量檢索與大型語言模型（LLM），能針對輸入問題自論文資料庫中擷取相關段落並生成回答。

## 📁 專案架構

```
.
├── RAG_main.ipynb
├── Dataset/
├── Experiment.pdf
├── requirements.txt
└── README.md
```

## 🚀 快速開始
可以在 Colab 上直接執行，若要在本機跑請按照下列步驟
### 安裝環境

```bash
python -m venv rag-env
source rag-env/bin/activate  # Windows: .\rag-env\Scripts\activate
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

### 執行 Notebook

```bash
jupyter notebook
```

打開 `RAG_main.ipynb` 執行主流程。

## 📦 requirements.txt

```text
pandas==2.2.3
jupyter==1.1.1
langchain==0.3.23
langchain-community==0.3.21
langchain-experimental
openai==1.71.0
faiss-gpu==1.7.2
numpy<2
rich==14.0.0
rouge-score
datasets
huggingface_hub
sentence-transformers
spacy
semantic-text-splitter
```

## 🔧 測試結果

- RougeL (chunks) = 0.2379
- Accuracy = 0.78
