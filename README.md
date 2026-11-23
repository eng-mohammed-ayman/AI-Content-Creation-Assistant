# AI-Driven Content Creation Assistant

An individual coursework prototype by Mohamed Ayman that routes a command-line prompt to text, image or video generation APIs. The original interface runs inside a Jupyter notebook and asks for content type, topic, tone and audience.

## Historical implementation

The source uses Google PaLM `models/text-bison-001` for blog posts/captions and Replicate models for Stable Diffusion images and Zeroscope video. These are the original provider integrations, not a claim that their old endpoints or SDK methods still work today. The legacy PaLM call needs migration to a currently supported text-generation API before a current end-to-end demo can be promised. Replicate model availability and versions also need verification with the provider.

Mohamed built the prototype, designed prompts, and debugged authentication, model-selection and request errors. This project is an API integration exercise, not a model trained from scratch.

## Inspect and run the historical notebook

```bash
python -m venv .venv
# Activate .venv.
pip install -r requirements.txt
export GOOGLE_API_KEY='your_own_key'
export REPLICATE_API_TOKEN='your_own_token'
jupyter lab content_creation_assistant.ipynb
```

Use equivalent environment-variable commands on Windows. The environment file is an example only and is not loaded automatically. Dependencies are historical and unpinned; this is not a tested lockfile. Read the notebook before running it. API calls may spend credits or money on your own provider account. No API calls were made during portfolio cleanup.

## Security and verification

Hardcoded Google and Replicate credentials were replaced with environment variables. All notebook outputs and execution metadata were cleared. The original report and slides are excluded because an embedded screenshot in the report exposes credentials. Removing credentials here does not revoke them; rotate exposed keys in the provider accounts.

The notebook structure and Python source have been checked, but current provider compatibility and generated outputs have not been verified. Do not treat this repository as a production-ready service.
