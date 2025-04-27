# ⚖️ AI Legal Team Agents

This Streamlit application provides a suite of AI-powered legal agents designed to assist with the analysis of legal documents. Upload your PDF document and interact with specialized agents to gain insights into contracts, conduct legal research, assess risks, and ensure compliance.

## ✨ Features

* **Multi-Agent Collaboration:** Utilizes a team of AI agents, including LegalAdvisor, ContractsAnalyst, LegalStrategist, and a Team Lead, to provide comprehensive analysis.
* **PDF Document Processing:** Accepts PDF files as input, processing and storing the content in a knowledge base for efficient retrieval.
* **Knowledge Base Integration:** Employs ChromaDB for vector storage and Gemini Embedder for semantic understanding of the document content.
* **Customizable Chunking:** Allows users to configure the chunk size and overlap for document processing.
* **Specialized Legal Agents:**
    * **LegalAdvisor:** Conducts legal research, finds relevant cases and regulations, and provides source references.
    * **ContractsAnalyst:** Reviews contracts to identify key clauses, risks, and obligations, referencing specific sections.
    * **LegalStrategist:** Assesses legal risks and opportunities, providing actionable recommendations and compliance guidance.
    * **Team Lead:** Integrates the responses from the other agents into a comprehensive legal analysis report.
* **Multiple Analysis Types:** Offers predefined analysis options such as Contract Review, Legal Research, Risk Assessment, Compliance Check, and a Custom Query option.
* **Structured Output:** Presents the analysis in a structured format with detailed findings, key points summary, and specific recommendations.
* **Web Search Capability:** Integrates DuckDuckGo for agents to fetch additional legal information when necessary.

## 🚀 App Demo

You can try out the live demo of the application here:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://legal-agent-mk.streamlit.app)

[Legal Agent](https://legal-agent-mk.streamlit.app)

## ⚙️ Dependencies

* `streamlit`: For creating the web application interface.
* `agno`: An AI agent framework for building intelligent agents.
* `python-dotenv`: For loading environment variables (like the API key).
* `google-generativeai`: The official Google Generative AI library.
* `chromadb`: A vector database for storing and querying embeddings.
* `pypdf`: A library for reading PDF files.

You can install all the necessary dependencies using the `requirements.txt` file (if provided).

## 🔑 Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/ai-legal-team-agents.git](https://github.com/your-username/ai-legal-team-agents.git)
    cd ai-legal-team-agents
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Set up Google API Key:**
    * Ensure you have a Google Cloud Project with the Generative AI API enabled.
    * Obtain an API key for the Generative AI service.
    * Run the Streamlit app. You will be prompted to enter your API key in the sidebar.

4.  **Run the Streamlit App:**
    ```bash
    streamlit run main.py
    ```
5.  **Configure Processing (Sidebar):**
    * Enter your Google API key.
    * Adjust the `Chunk Size` and `Overlap` for document processing as needed.
6.  **Upload Document (Sidebar):**
    * Click on "Browse files" and upload your legal document (PDF format).
7.  **Select Analysis Type:**
    * Choose the type of analysis you want to perform from the dropdown menu.
    * If you select "Custom Query", enter your specific legal question.
8.  **Analyze:**
    * Click the "Analyze" button to initiate the AI legal team.
9.  **View Results:**
    * The analysis will be presented in three tabs: "Analysis" (detailed findings), "Key Points" (summary), and "Recommendations" (actionable advice).

## 🧠 How It Works

This application utilizes the `agno` library to create a team of specialized AI agents that work collaboratively to analyze legal documents:

1.  **Document Processing:** The uploaded PDF document is read, and its content is chunked into smaller segments based on the configured chunk size and overlap.
2.  **Knowledge Embedding:** These chunks are then embedded using the `GeminiEmbedder` to create vector representations of their semantic meaning.
3.  **Vector Storage:** The embeddings are stored in the `ChromaDb` vector database, creating a searchable knowledge base.
4.  **AI Agent Interaction:** When a query is submitted:
    * The **LegalAdvisor** searches the knowledge base for relevant legal information and uses DuckDuckGo for external legal references.
    * The **ContractsAnalyst** focuses on identifying key clauses and obligations within the document.
    * The **LegalStrategist** assesses potential risks and provides strategic legal recommendations.
    * The **Team Lead**整合 the responses from the other agents into a comprehensive and structured report.

## ➕ Further Enhancements

* Support for more document types (e.g., DOCX, TXT).
* More granular control over agent instructions and parameters.
* Integration with legal databases and research platforms.
* User account management to save and track analyzed documents.
* Visualizations of key legal concepts and relationships within the document.

## 🙏 Contributing

Contributions to this project are welcome! Feel free to submit pull requests with bug fixes, new features, or improvements.

## 📄 License

[Your License Here (e.g., MIT License)](LICENSE)
