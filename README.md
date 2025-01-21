# Fyra: An Educational and Empathetic Document-Based Chatbot

Fyra is a Streamlit-based chatbot that processes various types of documents and provides personalized, educational, and empathetic responses to user queries. This chatbot is powered by the Cohere language model for natural language understanding and response generation.

## Features

- **Supports Multiple File Formats:**
  - Text (`.txt`)
  - PDF (`.pdf`)
  - Word Documents (`.docx`)
  - Excel Spreadsheets (`.xlsx`, `.xls`)
  - CSV Files (`.csv`)
  - PowerPoint Presentations (`.pptx`)
  - Images (`.jpg`, `.jpeg`, `.png`, `.tiff`)

- **Personalized Interactions:**
  - User name and gender are collected during onboarding for tailored responses.
  - Empathetic and educational tone in all responses.

- **Document Analysis:**
  - Extracts and processes content from uploaded files.
  - Answers user questions based on the extracted content.

- **Customizable Settings:**
  - Configurable Cohere API and Ngrok authentication tokens.

- **Ngrok Integration:**
  - Provides a public URL for easy access to the chatbot.

## Installation

### Prerequisites

Ensure you have the following installed:
- Python 3.8+
- Pip

Install the required Python libraries:
```bash
pip install streamlit cohere PyPDF2 pandas python-docx python-pptx pytesseract pillow pyngrok openpyxl
```

### Configuration

Create a `config.py` file with the following structure:
```python
config = {
    "COHERE_API_KEY": "your_cohere_api_key",
    "NGROK_AUTH_TOKEN": "your_ngrok_auth_token"
}
```

Replace `your_cohere_api_key` and `your_ngrok_auth_token` with your actual keys.

## Usage

1. **Run the Application:**
   ```bash
   python your_script_name.py
   ```

2. **Access the Application:**
   - Open the public URL provided by Ngrok (displayed in the terminal).

3. **Interact with Fyra:**
   - Enter your name and select your gender in the sidebar.
   - Upload a document.
   - Ask questions about the document.

## File Processing

Fyra can process and extract content from the following file types:
- **Text Files:** Reads plain text.
- **PDF Files:** Extracts text from all pages.
- **Excel Files:** Converts the content to a string.
- **CSV Files:** Parses and converts data into readable format.
- **Word Documents:** Extracts text from paragraphs.
- **PowerPoint Presentations:** Extracts text from slides.
- **Images:** Uses OCR (via Tesseract) to extract text from images.

## Code Overview

### Main Components

1. **File Parsers:**
   Functions to read and process supported file types (e.g., `read_pdf`, `read_docx`).

2. **Chatbot Response Function:**
   Generates responses using the Cohere API based on document content and user queries.

3. **Streamlit Application:**
   Provides the user interface for uploading documents, entering queries, and receiving responses.

4. **Ngrok Integration:**
   Publishes the application to a public URL for easy access.

## Example Interaction

1. User enters their name and gender.
2. Uploads a document (e.g., `example.pdf`).
3. Asks a question: "What are the main points in this document?"
4. Fyra processes the document and responds:
   ```
   The main points in the document are:
   - Point 1
   - Point 2

   Caution: This answer is for educational purposes. Please consult a professional for any additional information.
   ```

## Acknowledgements

- [Cohere](https://cohere.ai) for the natural language processing API.
- [Streamlit](https://streamlit.io) for the user interface.
- [Pyngrok](https://pyngrok.readthedocs.io/) for public URL access.

## Notes

- Ensure you have the necessary permissions to process uploaded files.
- The chatbot's responses are for educational purposes only and may require professional validation.



