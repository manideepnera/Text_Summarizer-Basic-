# AI Text Summarizer

An AI-powered Text Summarizer built using FastAPI and Google Gemini API.

This project allows users to paste large text content and generate concise AI summaries through a simple web interface.

---

## Features

- AI-powered text summarization
- FastAPI backend
- Gemini API integration
- HTML, CSS, and JavaScript frontend
- Simple and responsive UI
- Real-time summary generation
- REST API support

---

## Tech Stack

### Backend
- Python
- FastAPI
- Uvicorn
- Google GenAI SDK
- Python Dotenv
- Jinja2

### Frontend
- HTML
- CSS
- Vanilla JavaScript

---

## Project Structure

```txt
Text_Summarizer/
│
├── main.py
├── .env
├── requirements.txt
│
├── templates/
│   └── index.html
│
└── static/
    └── style.css
```

---

## Installation

### 1. Clone the Repository

```bash
git clone <your_repo_url>
cd Text_Summarizer
```

---

### 2. Create Virtual Environment

#### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

#### Mac/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install fastapi uvicorn google-genai python-dotenv jinja2
```

---

## Environment Variables

Create a `.env` file in the root directory.

```env
GEMINI_API_KEY=your_api_key_here
```

Get your API key from:

https://aistudio.google.com/app/apikey

---

## Running the Project

Start the FastAPI server:

```bash
uvicorn main:app --reload
```

Server runs at:

```txt
http://127.0.0.1:8000
```

---

## API Endpoints

### Home Route

```http
GET /
```

Loads the frontend UI.

---

### Summarize Route

```http
GET /summarize?text=your_text
```

#### Example

```txt
http://127.0.0.1:8000/summarize?text=Artificial%20Intelligence%20is%20a%20field...
```

#### Response

```json
{
  "summary": "Artificial Intelligence is a field of computer science focused on creating intelligent systems."
}
```

---

## Current Workflow

1. User enters text in the frontend textarea
2. Frontend sends request to FastAPI backend
3. FastAPI sends prompt to Gemini API
4. Gemini generates summary
5. Summary displayed in the UI

---

## Current UI Features

- Dark theme interface
- Large text input area
- Summary output section
- Interactive summarize button

---

## Future Improvements

- PDF summarizer
- File upload support
- Copy summary button
- Authentication system
- PostgreSQL database
- Summary history
- AI chat mode
- Streaming responses
- Mobile responsive optimization
- Docker deployment
- Railway deployment

---

## Dependencies

```txt
fastapi
uvicorn
google-genai
python-dotenv
jinja2
```

---

## License

This project is currently built for learning and development purposes.
