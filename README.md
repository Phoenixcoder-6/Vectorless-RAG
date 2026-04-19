# 📄 Vectorless RAG: Hierarchical Reasoning for Research Papers

## 🚀 The Problem with Traditional RAG

Most Retrieval-Augmented Generation (RAG) systems rely on Vector Embeddings. While powerful, they introduce several limitations:
### ❌ Lost Context
Chunking documents often breaks semantic flow and continuity.
### ❌ Flat Retrieval
Similarity search treats documents as independent chunks, ignoring hierarchical relationships (sections, subsections, etc.).
### ❌ Inefficient Reasoning
LLMs must infer relevance using distance metrics rather than structured understanding.

## 💡 The Solution: Vectorless (Tree-Based) RAG

This project implements a Vectorless RAG pipeline that replaces flat vector search with a Hierarchical Document Tree.
Instead of retrieving top-k similar chunks, an LLM navigates the document structure, mimicking how humans read:

    📚 From high-level summaries → to detailed sections → to precise answers

## 🛠️ Tech Stack

* Core Engine: PageIndex (document parsing & hierarchical indexing)
* LLM Inference: Groq / OpenAI
* Language: Python
* Environment: Jupyter Notebook
* Data: Research Papers (e.g., Spatial Pyramid Pooling in CNNs)

# 🏗️ How It Works

## 1️⃣ Automated Tree Construction

The system converts a PDF into a multi-level structure:

    Root: Document title & abstract
    Sections: Introduction, Methodology, Results
    Subsections: Fine-grained breakdown (e.g., 2.1, 2.2)
    Content Nodes: Paragraph-level text + summaries

## 2️⃣ Hierarchical Agentic Navigation

Instead of flat retrieval, the LLM:

    📖 Reads the root summary to understand context
    🎯 Selects the most relevant section
    🔍 Recursively drills down into subsections
    🧠 Maintains logical flow of the document

## 3️⃣ Context-Aware Generation

Because retrieval is structure-aware:

* The model understands where information comes from
* Maintains section-level context
* Produces more accurate and grounded answers

## 📊 Project Highlights
* 🚫 Zero Vector Dependency: No embeddings or vector databases required
* 🎯 High Precision Retrieval: Extracted deep insights from research papers (e.g., SPP-Net architecture)
* 🧠 Human-Like Reasoning: Navigation mimics how researchers explore documents
* 🔍 Explainable Outputs: Retrieval path is transparent (section → subsection → answer)

## 💻 System Workflow

<img width="841" height="538" alt="image" src="https://github.com/user-attachments/assets/8060ab2d-aa7b-4060-8500-76dc9cb4721e" />

## 👔 Recruitment Note

This project was built to explore next-generation RAG architectures.

While vector databases are widely used, hierarchical indexing + agentic reasoning provides a more interpretable and structured alternative—especially for:

* Legal documents
* Financial reports
* Research papers

## 🧑‍💻 Key Skills Demonstrated

* 🔹 RAG System Design: Traditional + Vectorless architectures
* 🔹 LLM Integration: Groq / OpenAI APIs
* 🔹 Prompt Engineering: Agentic navigation & reasoning
* 🔹 System Thinking: End-to-end pipeline design
* 🔹 Technical Communication: Translating complex IR concepts into working systems

##⭐ Final Insight

#### Vectorless RAG is not a replacement — I’s a step toward interpretable, reasoning-driven AI systems
