# Local AI Voice Agent (MVP)

A fully local, offline-capable AI assistant that controls your PC via voice or text.

## Setup

1. Install Python 3.10+
2. Install Ollama from https://ollama.ai
3. Pull a model: `ollama pull llama3.2`
4. Install dependencies: `pip install -r requirements.txt`

## Usage

**Text mode (recommended for testing):**
```
python -m ai_assistant.main --text
```

**Voice mode:**
```
python -m ai_assistant.main
```

## Supported Commands

- "Open notepad/calculator/browser/vscode"
- "Create folder at C:\Users\Ishaan\Documents\test"
- "Create a file at hello.py with print('hello')"
- "List files in Documents"
- "Read file at hello.py"
- "Run command dir"
- "What is the weather?" (uses LLM chat)

## Architecture

```
Voice Input (Whisper) → LLM Brain (Ollama) → Action Engine → System Execution
                                                       ↓
                                              Voice Output (pyttsx3)
```
