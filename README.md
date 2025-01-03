# 🤖 RockyBot: News Research Tool

A Streamlit-based application that allows users to analyze news articles using LangChain, Ollama, and Google's Gemini
model. The tool processes multiple URLs, creates embeddings, and answers questions about the content.

## 🌟 Features

- Process multiple news articles from URLs
- Create embeddings using Ollama
- Store vectors using FAISS for efficient retrieval
- Answer questions using Google's Gemini model
- Source attribution for answers
- User-friendly Streamlit interface

## 🔧 Prerequisites

- Python 3.8+
- Ollama running locally
- Google API key for Gemini
- Internet connection for URL processing

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/mustafoyev-202/RockyBot-News-Research-Tool-.git
cd rockybot
```

2. Create and activate a virtual environment:

```bash
conda create -n urlprocessor python=3.8
conda activate urlprocessor
```

3. Install required packages:

```bash
pip install streamlit
pip install langchain
pip install langchain-google-genai
pip install langchain-community
pip install python-dotenv
pip install faiss-cpu
pip install unstructured
```

4. Install and Start Ollama:
    - Visit [Ollama's website](https://ollama.ai/) to download
    - Install Ollama for your operating system
    - Start the Ollama server:
      ```bash
      ollama serve
      ```

5. Set up environment variables:
   Create a `.env` file in the project root:
   ```
   GOOGLE_API_KEY=your_google_api_key_here
   ```

## 🚀 Usage

1. Start the Streamlit application:

```bash
streamlit run main.py
```

2. Enter up to 3 news article URLs in the sidebar

3. Click "Process URLs" to analyze the content

4. Ask questions about the articles in the main input field

## 💡 How It Works

1. **URL Processing**
    - Loads content from provided URLs
    - Splits text into manageable chunks
    - Creates embeddings using Ollama

2. **Vector Storage**
    - Stores embeddings in FAISS index
    - Saves index to disk for persistence
    - Enables efficient retrieval

3. **Question Answering**
    - Uses Google's Gemini model
    - Retrieves relevant context using FAISS
    - Provides sourced answers

## 🛠️ Configuration

You can modify these parameters in `main.py`:

```python
# Chunk size for text splitting
chunk_size = 1000

# Temperature for Gemini model
temperature = 0.9

# Number of URLs (currently set to 3)
```

## 📈 Performance Tips

1. Adjust chunk size based on your needs
2. Use fewer URLs for faster processing
3. Consider reducing model temperature for more focused answers

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## 👥 Authors

Name - baxtiyormustafoyev2006@gmail.com

## 🙏 Acknowledgments

- LangChain team
- Ollama project
- Google Gemini team
- Streamlit developers

## 📞 Support

For support, please open an issue in the GitHub repository or contact the maintainers.