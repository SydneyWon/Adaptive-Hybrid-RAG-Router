# 🚦 Adaptive Hybrid RAG Router: Cost-Efficient Agentic Orchestration

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Libraries](https://img.shields.io/badge/Libraries-LangChain%20%7C%20Neo4j%20%7C%20Chroma-orange)
![Models](https://img.shields.io/badge/Models-DistilBERT%20%7C%20GPT--4o-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

> **"An intelligent Agentic RAG framework that optimizes performance-to-cost ratios by utilizing Knowledge Distillation to route complex queries between Vector and Graph databases."**

- **Problem:** Standard RAG systems often fail at complex, multi-hop reasoning and incur prohibitive API costs/latency when relying solely on high-end LLMs for all queries.

- **Solution:** Developed an Agentic Router by distilling GPT-4’s reasoning (CoT) into a lightweight DistilBERT model. The system dynamically routes requests to either Vector RAG (Chroma) or GraphRAG (Neo4j) based on query complexity.
  
- **Impact:** Achieved 98.3% routing accuracy while reducing inference latency to milliseconds and significantly lowering operational costs for enterprise-scale deployment.

---

## 📌 Project Overview
This project implements an advanced Agentic AI Orchestrator designed for complex domains (e.g., Theology, Legal, Finance) where data relationships are as critical as the raw text. 
By integrating a hybrid retrieval infrastructure, the system ensures that simple factual questions are handled efficiently by Vector search, while intricate relational queries are resolved through Knowledge Graphs.

### **Key Objectives**  
1.  **System Efficiency:** Minimize reliance on expensive LLM calls by using a specialized small-scale router.
2.  **Reasoning Depth:** Enable Multi-hop reasoning via Neo4j GraphRAG for entities with implicit connections.
3.  **Knowledge Distillation:** Transfer high-level cognitive logic from a Teacher model (GPT-4) to a Student model (DistilBERT).

---

## 🛠️ Tech Stack
* **Orchestration:** LangChain (Agentic Workflows)
* **Models:** GPT-4o (Reasoning Teacher), DistilBERT (Real-time Router)
* **Storage:** Neo4j (Graph Database), ChromaDB (Vector Database)
* **Optimization:** Knowledge Distillation, Chain-of-Thought (CoT) Prompting
* **Data Engineering:** Python, PySpark, Azure ML, Docker

---

## 📂 Dataset & Methodology
* **Core Data:** Compendium of the Catechism of the Catholic Church.
* **Preprocessing:** Handled OCR errors (e.g., missing IDs 434, 568) and utilized Regex-based cleaning to ensure high-fidelity, ML-ready data. 
* **Synthetic Data Generation:** Leveraged GPT-4o-mini to generate a balanced dataset of 1,795 high-quality synthetic queries categorized into three distinct routing labels.

---

## 🔍 Key Features
### 1. Dual-RAG Infrastructure
* **Vector RAG:** Utilizes text-embedding-3-small for semantic similarity search in ChromaDB.
* **GraphRAG:** Employs GPT-4o as a data engineer to extract entities and relationships (e.g., INSTITUTED_BY), enabling relational path-finding in Neo4j.

### 2. Distilled Adaptive Router
A fine-tuned DistilBERT model serves as the gateway, classifying user intent with extreme low-latency. It identifies whether a query requires simple retrieval, complex graph-traversal, or is out-of-scope.

### 3. Agentic Prompting
Utilizes CoT (Chain-of-Thought) patterns to ensure the AI agent reasons through the retrieved context before generating the final response.

--- 

## 📊 Results Summary

| Metric | DistilBERT Router |
| :--- | :---: |
| **Accuracy** | 98.3% |
| **Inference Latency** |  |
| **API Cost** |  |

> **Business Impact:**

---

## ⚖️ Strategic Value & XAI

In a regulated enterprise environment, black-box AI is a risk. This project emphasizes:
* **Explainable Routing:** Every decision to use Vector or Graph search is logged with a rationale, providing an audit trail for system behavior.
* **Resource Efficiency:** By offloading "thinking" tasks to smaller models, we ensure the infrastructure is scalable without linear cost growth. 

---

## 👤 Author
* **Name:** Sydney Won
* **Contact:** sydney.b.won@gmail.com
* **Portfolio:** www.github.com/SydneyWon

---
*This project is for educational and portfolio purposes.*
