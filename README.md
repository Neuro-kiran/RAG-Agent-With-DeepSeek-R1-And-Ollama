# RAG-Agent With DeepSeek R1 And Ollama

## Overview
This project implements a **Retrieval-Augmented Generation (RAG) Agent** leveraging **DeepSeek R1** and **Ollama** to efficiently retrieve and generate answers based on document content. The agent processes large PDFs, extracts relevant information, and generates structured responses.

## Features
- **PDF Processing**: Extracts text from PDFs and converts it into a searchable format.
- **DeepSeek R1 Integration**: Utilizes DeepSeek R1 for retrieval-based answering.
- **Ollama for Generation**: Uses Ollama models to enhance response generation.
- **Efficient Query Handling**: Structured JSON output with high-confidence answers.
- **Slack Integration** (Optional): Posts answers to Slack channels.

## Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- `pip` package manager
- `virtualenv` (optional but recommended)

### Clone the Repository
```bash
git clone https://github.com/Neuro-kiran/RAG-Agent-With-DeepSeek-R1-And-Ollama.git
cd RAG-Agent-With-DeepSeek-R1-And-Ollama
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Set Up Environment Variables
Create a `.env` file and add the required API keys:
```
DEEPSEEK_API_KEY=your_deepseek_api_key
OLLAMA_API_KEY=your_ollama_api_key
SLACK_BOT_TOKEN=your_slack_token  # Optional
```

## Usage

### Running the Agent
```bash
python app.py
```

### Upload a PDF
- Place your PDF file (e.g., `document.pdf`) in the `data/` folder.
- The agent processes the PDF and retrieves answers based on queries.

### Example API Request
```bash
curl -X POST "http://localhost:5000/query" \
     -H "Content-Type: application/json" \
     -d '{"question": "What is the main topic of the document?"}'
```

### Example Response
```json
{
  "question": "What is the main topic of the document?",
  "answer": "The document primarily discusses AI-driven automation techniques."
}
```

## Future Enhancements
- Implement vector database support for optimized retrieval.
- Enhance response accuracy with additional fine-tuned models.
- Extend integration with other LLM frameworks.

## Contributing
Feel free to fork this repository and submit pull requests with improvements.

## License
This project is licensed under the MIT License.

