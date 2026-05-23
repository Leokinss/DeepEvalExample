# DeepEval Example

A small example project demonstrating [DeepEval](https://github.com/confident-ai/deepeval), an open-source LLM evaluation framework for Python.

## What this shows

- Running built-in metrics (answer relevancy, faithfulness, hallucination) against LLM outputs
- Writing evaluation cases with `LLMTestCase`
- Running evaluations as `pytest`-style tests

## Setup

1. Create and activate a virtual environment:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

2. Install dependencies:

   ```powershell
   pip install -r requirements.txt
   ```

3. Copy `.env.example` to `.env` and add your OpenAI API key (DeepEval uses an LLM judge by default):

   ```powershell
   Copy-Item .env.example .env
   ```

## Running

Run the standalone example script:

```powershell
python example.py
```

Or run the pytest-style evaluation:

```powershell
deepeval test run test_example.py
```

## Project layout

- `example.py` — minimal standalone evaluation using `evaluate()`
- `test_example.py` — pytest-style evaluation using `assert_test`
- `requirements.txt` — pinned dependencies
- `.env.example` — template for required environment variables
