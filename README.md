# Agentic-RAG-AI-Tutor

An AI Math Tutor that explains solutions step by step using a Retrieval-Augmented Generation (RAG) pipeline and an agentic loop. It prioritizes answers from a curated knowledge base, falls back to safe web/MCP search if needed, and learns from feedback.

## Features
- **Step-wise explanations**: Produces clear, structured math solutions.
- **RAG-first**: Searches a vetted dataset before generating answers.
- **Safe fallback**: Optionally queries the web/MCP with guardrails and citations.
- **Feedback loop**: Captures user feedback to improve future responses.

## Project Structure
```
backend/
  app/
    agent.py           # Agent orchestration (RAG + web/MCP + feedback)
    config.py          # Settings/env loading (API keys, feature flags)
    dspy_feedback.py   # Feedback capture & DSPy/LLM alignment hooks
    guardrails_config.py # Safety policies / content filters
    main.py            # FastAPI app entrypoint
    models.py          # Pydantic request/response models
    utils.py           # Common helpers
    vector_store.py    # In-memory / local vector store utilities
    data/dataset.json  # Curated KB
frontend/
  index.html           # Minimal UI to ask questions and view answers
```

