# VoiceBot — GPT-style Assistant

A simple web-based voice bot using a Python backend (Flask) and a Groq API integration.  
It supports **voice input**, **text input**, and **speaks the response aloud**.

---

## Features

- Speak naturally or type your question.
- Bot responds using your Groq API (or any backend AI API).
- Response is **spoken aloud** using browser TTS.
- Stop voice output at any time using **Stop Response**.
- Minimal, clean UI — works in modern browsers (Chrome/Edge recommended).

---

## Setup Instructions

### 1. Clone the project

```bash
git clone <your-repo-url>
cd <project-folder>
```

### 2. Create a Conda environment

```bash
conda create -n 100x python=3.11 -y
conda activate 100x
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure your environment variables

Create a `.env` file in the project root:

```text
GROQ_API_KEY=your_groq_api_key_here
```

### 5. Run the backend server

```bash
python server.py
```

By default, the server runs on `http://localhost:8001`.

---

### 6. Open the frontend

Open `index.html` in a modern browser.  
- Click **Start Listening** or type a question.  
- Click **Ask** to get a response.  
- Use **Stop Response** to stop voice and clear reply.

---

## Notes

- Ensure your browser supports the **Web Speech API** for speech recognition and synthesis.  
- Recommended: Chrome or Edge.  
- No API key needed for the frontend itself; backend requires your Groq API key.

---

## Troubleshooting

- **Port 8001 already in use**: Change the port in `server.py`:
  ```python
  app.run(port=8002, debug=True)
  ```
- **Speech not working**: Check microphone permissions and browser compatibility.  
- **Backend errors**: Check terminal logs for API request issues.

---

## License

MIT License

