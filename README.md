# Code Review Assistant

## What it does
Automates code reviews using an LLM to analyze code quality, modularity, security, and tests; returns actionable JSON reports.

## Quickstart (dev)
1. `git clone ...`
2. `python -m venv venv && source venv/bin/activate`
3. `pip install -r requirements.txt`
4. `export OPENAI_API_KEY=...`
5. `uvicorn app.main:app --reload`

## API
POST /api/review (multipart/form-data: files[])

## Output
JSON report with file-level issues and overall scores.

## Notes
- For large repos use `POST /api/review-from-git` to review selective folders.
- Keep LLM prompt template in `app/llm_prompts.py`.
  
