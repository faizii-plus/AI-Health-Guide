
# 🩺 AI Health Guide

An AI-powered health-information assistant built with Python,
Streamlit, and the OpenAI API.

## 1. Project Overview

AI Health Guide helps users understand general health information
in a simple conversational interface.

It is designed as an educational prototype and does not diagnose
diseases, prescribe medication, or replace qualified healthcare
professionals.

## 2. Features

- Interactive AI chat interface
- English and Urdu response options
- General health education
- Nutrition, sleep, and wellness information
- Medical terminology explanations
- Help preparing questions for a doctor
- Basic emergency-warning phrase checks
- API error handling
- Conversation clearing
- API key configuration through environment variables
  or Streamlit secrets

## 3. Technology Stack

- Python 3.10 or newer
- Streamlit
- OpenAI Python SDK
- OpenAI Responses API

## 4. Project Structure

Create a folder named `ai-health-guide`:

    ai-health-guide/
    ├── app.py
    ├── README.md
    └── requirements.txt

## 5. Installation

### Step 1: Install Python

Install Python 3.10 or newer from:

https://www.python.org/downloads/

Verify your installation:

    python --version

### Step 2: Open the project folder

Open a terminal or command prompt inside the project folder.

### Step 3: Create a virtual environment

Windows:

    python -m venv .venv
    .venv\Scripts\activate

macOS or Linux:

    python3 -m venv .venv
    source .venv/bin/activate

### Step 4: Install dependencies

    python -m pip install -r requirements.txt

## 6. Configure the OpenAI API Key

You need an OpenAI API key for AI-generated responses.

Get your key from:

https://platform.openai.com/api-keys

API usage may incur charges. API access and ChatGPT subscriptions
are separate; check your API account's billing and usage limits.

### Option A: Set an environment variable

Windows PowerShell:

    $env:OPENAI_API_KEY="your-api-key"

macOS or Linux:

    export OPENAI_API_KEY="your-api-key"

Replace the example value with your actual key. Never share your
key or commit it to a public repository.

### Option B: Use Streamlit secrets

Create a folder named `.streamlit` in the project directory.
Inside it, create `secrets.toml`:

    OPENAI_API_KEY = "your-api-key"

Keep this file private and do not upload it to GitHub.

## 7. Run the Application

In the activated virtual environment, run:

    streamlit run app.py

Streamlit will provide a local URL, usually:

    http://localhost:8501

Open that address in your web browser.

## 8. Choose an AI Model

The default model is configured in `app.py`.

You can override it with the `OPENAI_MODEL` environment variable
if you have access to another compatible model.

Windows PowerShell:

    $env:OPENAI_MODEL="your-available-model"
    streamlit run app.py

macOS or Linux:

    export OPENAI_MODEL="your-available-model"
    streamlit run app.py

Use a model name supported by your API account.

## 9. Example Questions

- What is dehydration?
- What are healthy sleep habits?
- Explain blood pressure in simple language.
- What questions should I ask my doctor about a new prescription?
- What are general ways to maintain a balanced diet?

For Urdu, choose Urdu from the language selector.

## 10. Safety and Limitations

This project is an educational prototype, not a validated
clinical decision-support system.

- AI responses can be incorrect or incomplete.
- Emergency phrase checks are limited and may miss dangerous
  symptoms or flag phrases that are not emergencies.
- A warning check is not a medical triage system.
- Do not use this app to diagnose or treat medical conditions.
- Do not use it to determine medication doses or change
  prescribed treatment.
- Seek qualified medical care for concerning symptoms.
- For emergencies, contact local emergency services immediately.

The application does not intentionally save chat history to a
database. However, messages sent to an AI API are transmitted to
that service and may be processed under its applicable policies.
Do not enter identifying or sensitive medical information.

Before public deployment, implement privacy controls, secure
logging practices, rate limits, stronger emergency handling,
and clinical safety evaluation.

## 11. Future Improvements

- Add speech input and text-to-speech.
- Add support for additional local languages.
- Provide verified health-resource references.
- Build a medically reviewed knowledge base.
- Add accessibility features.
- Conduct safety testing with qualified healthcare professionals.

## 12. License

Choose an appropriate license before distributing this project.

---

Created as an educational AI project.
