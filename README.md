# AI Assistant Flask App

This is a simple Flask-based AI assistant using OpenAI and Perplexity APIs.

## Requirements
- Python 3.8+
- pip
- (Optional) Docker

## Setup

### 1. Clone the repository
```bash
git clone https://github.com/QianqianQ/ai-chat.git
cd ai-assistant
```

### 2. Create and activate a virtual environment (recommended)
```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up environment variables
```
cp .env.example .env
# Then edit .env to add your real SONAR_API_KEY
```

## Running Locally
```bash
flask run
```
The app will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000)

## Running with Docker

### 1. Build the Docker image
```bash
docker build -t ai-assistant .
```

### 2. Run the container (using your local .env file)
```bash
docker run --env-file .env -p 5000:5000 ai-assistant
```

The app will be available at [http://localhost:5000](http://localhost:5000)

---

## Endpoints
- `GET /` — Health check
- `POST /ask` — Ask a question (JSON: `{ "prompt": "your question" }`)

---

## Notes
- Do **not** commit your `.env` file to version control.
- For development, you can use the provided `launch.json` for VS Code debugging.
