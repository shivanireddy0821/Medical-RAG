# Medical-RAG

# Overview #
Medical-RAG is an intelligent information retrieval system that leverages Retrieval-Augmented Generation (RAG) to provide medical insights from structured and unstructured text data.
The project uses Groq’s Llama-3.1-8B-Instant model for language understanding and Pinecone as the vector database for fast and accurate document retrieval.
A Flask frontend is used to create an interactive interface for users to query the system.

---

# Data Source #
The dataset used in this project is derived from a medical reference book containing information about various diseases, their symptoms, precautions, and treatments.
The text data from the book is processed and stored in Pinecone to enable efficient retrieval and context-aware responses.

---

# Project Architecture #

Data Processing

The medical book data is cleaned, preprocessed, and embedded into vector representations.
Embeddings are stored in Pinecone DB for semantic search and retrieval.

Retriever-LLM Integration

When a user asks a question, the retriever fetches the most relevant sections from the Pinecone database.
These retrieved documents are passed to the Groq Llama-3.1-8B-Instant model for generating accurate and context-rich responses.

Frontend Interface

The system uses Flask to provide a user-friendly web interface.
Users can enter their medical questions, view AI-generated responses, and understand related diseases or treatments.

---

# Key Features #
Retrieves reliable medical information based on user queries.
Uses vector search for efficient retrieval of relevant content.
Provides contextual and human-like explanations using an LLM.
Built with a modular architecture for easy extension to other domains.

---

# How It Works? #
User enters a medical query in the Flask web interface.
The query is converted into an embedding and compared with the Pinecone index.
Relevant text chunks from the medical data are retrieved.
These chunks are passed to the Groq Llama model for generating the final answer.
The response is displayed on the frontend.

---

# Technology Stack #

| Component           | Technology                                        |
| ------------------- | ------------------------------------------------- |
| **Language Model**  | Groq Llama-3.1-8B-Instant                         |
| **Vector Database** | Pinecone                                          |
| **Framework**       | Flask                                             |
| **Core Libraries**  | LangChain, LangChain-Groq, Pinecone-client, Flask |

---


## 🚀 Quick Start

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/shivanireddy0821/Medical-RAG.git
cd Medical-RAG
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # For macOS/Linux
venv\Scripts\activate      # For Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Set Up Environment Variables

Create a `.env` file in the project root and add your keys:

```
GROQ_API_KEY=your_groq_api_key
PINECONE_API_KEY=your_pinecone_api_key
```

### 5️⃣ Run the Application

```bash
python app.py
```

Then open your browser and visit:

```
http://127.0.0.1:5000
```

---

# Future Enhancements #

* Add support for multiple medical datasets.
* Add chat history and context memory
* Improve UI using Tailwind CSS or React frontend
* Integrate speech-to-text and text-to-speech modules
* Add confidence score and source reference for transparency
* Deploy on a cloud service for public access.

---

