# CV-AI-AGENT 

A personal AI agent that acts as a digital twin, capable of answering questions about my professional background, skills, and experience.

## Features

- **Personalized Interaction**: Representing me (Amith C M) faithfully using context from my CV and summary.
- **Smart Knowledge Retrieval**: Uses OpenAI GPT-4o-mini to process and answer queries based on a PDF CV and a text summary.
- **Lead Capture**: Automatically asks for and records user contact details when they show interest.
- **Question Tracking**: Records questions that the AI cannot answer to help me improve its knowledge base.
- **Real-time Notifications**: Integrated with **Pushover** to send instant alerts whenever a user leaves their details or asks an unknown question.
- **Modern UI**: Clean and interactive chat interface built with **Gradio**.

## Live Demo

You can interact with my AI Agent here:
[Hugging Face Space: CV-AI-AGENT](https://huggingface.co/spaces/cmamith/CV-AI-AGENT)

## Tech Stack

- **Large Language Model**: OpenAI GPT-4o-mini
- **Frontend Framework**: Gradio
- **PDF Processing**: PyPDF
- **Notifications**: Pushover API
- **Environment Management**: Python `dotenv`

## ⚙️ Setup & Installation

### 1. Prerequisites
- Python 3.8+
- An OpenAI API Key
- A Pushover User Key and API Token (optional, for notifications)

### 2. Clone the Repository
```bash
git clone https://github.com/cmamith/CV-AI-AGENT.git
cd CV-AI-AGENT
```

### 3. Create a Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Configure Environment Variables
Create a `.env` file in the root directory:
```env
OPENAI_API_KEY=your_openai_api_key
PUSHOVER_TOKEN=your_pushover_app_token
PUSHOVER_USER=your_pushover_user_key
```

### 6. Add Your Content
- Replace `me/CV.pdf` with your own resume in PDF format.
- Update `me/summary.txt` with a brief text-based bio.

### 7. Run Locally
```bash
python3 app.py
```
The interface will be available at `http://127.0.0.1:7860`.

## 🚢 Deployment (Hugging Face Spaces)

This project is optimized for deployment on Hugging Face Spaces using the Gradio SDK.

```bash
uv run gradio deploy
```

Make sure to add `OPENAI_API_KEY`, `PUSHOVER_TOKEN`, and `PUSHOVER_USER` as **Secrets** in your Hugging Face Space settings.

