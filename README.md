
# T5 Text Summarizer

An abstractive text summarization application built using **T5 (Text-to-Text Transfer Transformer)**, PyTorch, Hugging Face Transformers, and FastAPI. The application generates concise summaries from lengthy text or conversations through a simple web interface.

## Project Overview

Text summarization is an important Natural Language Processing (NLP) task that reduces lengthy text into shorter versions while preserving the key information.

This project uses a fine-tuned T5-small model to generate meaningful summaries from input text. A FastAPI backend connects the trained model to an HTML-based frontend, allowing users to enter text and receive generated summaries.

## Features

- Abstractive text summarization using T5-small.
- Fine-tuning with the SAMSum dataset.
- Text preprocessing and tokenization.
- Beam search-based text generation.
- FastAPI backend for model inference.
- Simple and user-friendly HTML interface.
- REST API endpoint for generating summaries.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| PyTorch | Deep learning framework |
| Hugging Face Transformers | T5 model implementation |
| T5-small | Text summarization model |
| SAMSum Dataset | Training and validation data |
| FastAPI | Backend API development |
| HTML, CSS, JavaScript | Frontend development |
| Jupyter Notebook | Model training and experimentation |

## Project Workflow

1. Load the SAMSum dataset.
2. Preprocess and clean the dialogue text.
3. Tokenize input dialogues and target summaries using the T5 tokenizer.
4. Fine-tune the T5-small model using the training dataset.
5. Evaluate the model on validation data.
6. Save the trained model and tokenizer.
7. Integrate the trained model with FastAPI.
8. Build a web interface to accept input text and display generated summaries.

## Project Structure

```text
Text-Summarizer/
│
├── app.py
├── index.html
├── requirements.txt
├── text_summerization.ipynb
├── README.md
│
└── screenshots/
    ├── homepage.png
    ├── generated_summary.png
    └── api_docs.png
```

**Note:** The trained model folder (`saved_summary_model_v2`) is not included in this repository because of its large file size.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Text-Summarizer.git
cd Text-Summarizer
```

### 2. Create a Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up the Trained Model

The trained model is not included in this repository.

To run the application, obtain the trained T5 model and tokenizer files and place them inside:

```text
saved_summary_model_v2/
```

The folder should contain the model configuration, model weights, and tokenizer files generated during training.

The model path in `app.py` should point to this directory.

### 5. Run the Application

```bash
uvicorn app:app --reload
```

Open your browser and visit:

```text
http://127.0.0.1:8000
```

## API Documentation

FastAPI provides interactive API documentation.

After starting the application, visit:

```text
http://127.0.0.1:8000/docs
```

### API Endpoint

**POST** `/summarize/`

Example request:

```json
{
  "dialogue": "Artificial intelligence is transforming various industries. Companies are using machine learning to automate tasks and improve decision-making."
}
```

Example response:

```json
{
  "summary": "Artificial intelligence is transforming industries through machine learning and automation."
}
```

*The response above is illustrative; actual summaries depend on the input and trained model.*

## Screenshots

### Web Application

Add your application homepage screenshot here.

```text
![Homepage](screenshots/homepage.png)
```

### Generated Summary

Add a screenshot showing the generated summary.

```text
![Generated Summary](screenshots/generated_summary.png)
```

### API Documentation

Add a screenshot of the FastAPI Swagger documentation.

```text
![API Documentation](screenshots/api_docs.png)
```

## Model Information

- **Architecture:** T5 (Text-to-Text Transfer Transformer)
- **Model:** T5-small
- **Task:** Abstractive Text Summarization
- **Dataset:** SAMSum
- **Training Framework:** PyTorch
- **Model Library:** Hugging Face Transformers

## Future Improvements

- Add ROUGE-based evaluation metrics.
- Improve summary fluency and factual consistency.
- Support larger text inputs.
- Improve frontend design and user experience.
- Deploy the application to a cloud platform.

## Learning Outcomes

Through this project, I gained practical experience in:

- Natural Language Processing.
- Transformer-based deep learning models.
- Fine-tuning pretrained language models.
- Text preprocessing and tokenization.
- Model inference using PyTorch and Hugging Face.
- Building REST APIs using FastAPI.
- Integrating machine learning models with web applications.

