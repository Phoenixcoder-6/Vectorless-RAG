📄 Vectorless RAG: Hierarchical Reasoning for Research Papers
🚀 The Problem with Traditional RAG
Most RAG (Retrieval-Augmented Generation) systems rely on Vector Embeddings. While powerful, they often struggle with:

Lost Context: "Chunking" documents often breaks the semantic flow.

Flat Retrieval: Similarity search treats a document as a bag of chunks, losing the hierarchical relationship between sections, subsections, and paragraphs.

Inefficient Reasoning: LLMs must "guess" which chunks are relevant based on a simple distance metric.

💡 The Solution: Vectorless (Tree-Based) RAG
This project implements a Vectorless RAG pipeline that replaces the "flat" vector database with a Hierarchical Document Tree. Instead of searching for similar vectors, an LLM agent navigates the actual structure of the document—moving from high-level summaries to specific technical details—mimicking how a human researcher reads a paper.

🛠️ Tech Stack
Core Engine: PageIndex (Automated document tree construction and hierarchical search).

Inference: Groq / OpenAI (Handling reasoning and final generation).

Data Processing: Python, Jupyter Notebook.

Target Data: Complex Research Papers (e.g., Spatial Pyramid Pooling in Deep Convolutional Networks).

🏗️ How it Works
1. Automated Tree Construction
The system ingests a PDF and parses its layout into a multi-level tree:

Root: Document Title & Abstract.

Sections: Introduction, Methodology, Results, etc.

Subsections: Detailed technical breakdowns (e.g., Section 2.1 vs 2.2).

Content Nodes: The raw text and summaries of specific paragraphs.

2. Hierarchical Agentic Navigation
Instead of fetching the "top-k" chunks, the agent:

Reads the Root Summary: Understands the overall scope of the paper.

Identifies Target Sections: Decides which section (e.g., "3.2 Experiments") is most likely to contain the answer.

Drills Down: Navigates only to relevant subsections, maintaining full context of the document's logic.

3. Context-Aware Generation
By traversing the tree, the LLM maintains the structural context. It knows that the data it is reading belongs to a specific table or section, leading to significantly higher accuracy in technical queries.

📊 Project Highlights
Zero-Vector Setup: No need for complex embedding models or memory-heavy vector databases.

High Precision: Successfully extracted deep architectural details from the SPP-Net paper, such as how Spatial Pyramid Pooling replaces fixed-size pooling layers (like pool5) to handle arbitrary input sizes.

Human-Like Reasoning: The chat agent explains where in the hierarchy it found the information, providing better transparency than traditional "black-box" vector search.

💻 System Workflow
Code snippet
graph TD
    A[User Query] --> B[LLM-based Section Selection]
    B --> C[Hierarchical Tree Traversal]
    C --> D[Relevant Node Extraction]
    D --> E[Answer Generation]
    
👔 Recruitment Note
I built this project to explore the frontiers of Agentic RAG. While vector databases are the industry standard, hierarchical indexing represents the next step in making LLMs truly understand structured data like legal documents, financial reports, and technical research papers.

Key Skills Demonstrated:

RAG Architecture: Advanced knowledge of both Traditional and Tree-based methods.

API Integration: Hands-on experience with PageIndex and Groq.

Prompt Engineering: Designing logic for Agentic Navigation.

Technical Communication: Bridging complex IR concepts with functional code.
