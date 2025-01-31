# AI-Powered Doc Crawler

An **AI-powered document search and Q&A system** designed to help users efficiently retrieve information from large document repositories. This project leverages **LangChain**, **ChromaDB**, **HuggingFace embeddings**, and **Ollama models** to perform intelligent searches across documents and provide concise answers to user queries.

---

## Features

- **Document Crawling:** Automatically scans and indexes multiple documents, creating a searchable vector space.
- **AI-Powered Search:** Uses embeddings and vector similarity to retrieve the most relevant content.
- **Natural Language Q&A:** Provides natural language responses to user queries based on document context.
- **Interactive Chat UI:** Built with Chainlit, allowing users to interact seamlessly through a web-based interface.
- **Model Backend:** Utilizes local LLMs from **Ollama** for generating responses.

---

## Requirements

Ensure you have the following installed:

- **Python 3.11+**
- **Java (for BFG Repo Cleaner)**
- **Git**
- **Ollama CLI**
- **Homebrew (for macOS)**

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/vineethsaivs/AI-Powered-Doc-Crawler.git
   cd AI-Powered-Doc-Crawler
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # For Linux/macOS
   # On Windows: .\venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Install and set up Ollama:**
   Install the Ollama CLI using Homebrew:
   ```bash
   brew install --cask ollama
   ollama serve  # Start the server
   ```

5. **Download the required models using Ollama:**
   ```bash
   ollama pull phi4
   ```

---

## Project Structure

```
AI-Powered-Doc-Crawler/
│
├── base_test/                   # Contains test files for validation
├── crawler.py                   # Logic for crawling and indexing documents
├── main.py                      # Main application logic for handling queries
├── requirements.txt             # Python dependencies
├── chainlit.md                  # Chainlit configuration for the chat interface
├── .gitattributes               # LFS tracking configuration
├── README.md                    # Project documentation
├── vectorstore/                 # Stores ChromaDB vectors
└── .gitignore                   # Ignored files and directories
```

---

## Running the Application

1. **Start the Ollama server:**
   ```bash
   ollama serve
   ```

2. **Run the Chainlit application:**
   ```bash
   python -m chainlit run main.py
   ```

3. **Access the interface:**
   - Open your browser and visit: [http://localhost:8000](http://localhost:8000)

4. **Ask questions based on indexed documents:**
   - Upload documents as needed, and the system will generate answers using AI-powered search.

---

## Cleaning the Git History (For Contributors)

During development, we cleaned the Git history and large files using **BFG Repo Cleaner** and **Git LFS**.

### Steps we followed:
1. **Install Git LFS:**
   ```bash
   git lfs install
   git lfs track "*.dylib" "*.so" "*.bin" "node" "libtorch_cpu.dylib"
   ```

2. **Use BFG to clean large files:**
   ```bash
   java -jar bfg.jar --delete-files '*.dylib' '*.so' 'libtorch_cpu.dylib' 'node' '*.bin'
   ```

3. **Expire and garbage collect old commits:**
   ```bash
   git reflog expire --expire=now --all
   git gc --prune=now --aggressive
   ```

4. **Force push the clean repo:**
   ```bash
   git push origin main --force
   ```

---

## Key Technologies

- **LangChain:** Framework for building chains of LLM-powered components.
- **ChromaDB:** Vector database for indexing and searching document embeddings.
- **HuggingFace Embeddings:** Generates document embeddings for semantic search.
- **Ollama:** LLM engine for local inference and chat completions.
- **Chainlit:** Interactive web-based UI for user interactions.

---

## Troubleshooting

### 1. Large File Issues in Git
If you encounter issues with large files during Git operations, ensure Git LFS is properly set up and the history is cleaned using BFG as described in the **Cleaning the Git History** section.

### 2. Ollama Server Connection Issues
- Make sure the Ollama server is running using `ollama serve`.
- Ensure the correct port is configured (default: 11434).

---

## Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request. Ensure your changes follow the project’s coding standards and are thoroughly tested.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- **LangChain** for providing a modular framework to build AI-powered applications.
- **Ollama** for efficient local LLM inference.
- **HuggingFace** for state-of-the-art embeddings.
- **Chainlit** for a clean and responsive chat UI.

---

## Contact
For any questions or suggestions, please reach out through the GitHub repository: [AI-Powered Doc Crawler](https://github.com/vineethsaivs/AI-Powered-Doc-Crawler).
