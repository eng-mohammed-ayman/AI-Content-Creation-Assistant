# AI-Driven Content Creation Assistant

An individual coursework prototype by Mohamed Ayman: a multi-modal generative AI assistant supporting 3 modalities (text, image, video) across 4 content formats (blog posts, social media captions, images, videos) by integrating 2 APIs (Google PaLM text-bison-001 and Replicate API) with Stable Diffusion and Zeroscope-v2-xl. The original interface runs inside a Jupyter notebook and asks for content type, topic, tone and audience.

## Historical implementation

The source uses Google PaLM `models/text-bison-001` for blog posts/captions and Replicate models for Stable Diffusion images and Zeroscope video. These are the original provider integrations.

Mohamed built the prototype and engineered dynamic text prompts parameterized by 4 user inputs (content type, topic, tone, target audience) with 0.7 temperature and 500-token output limits. He resolved 5 API authentication, model-selection and runtime bugs, validating the pipelines with unit and end-to-end integration tests. This project is an API integration exercise, not a model trained from scratch.

## Inspect and run the historical notebook

```bash
python -m venv .venv
# Activate .venv.
pip install -r requirements.txt
export GOOGLE_API_KEY='your_own_key'
export REPLICATE_API_TOKEN='your_own_token'
jupyter lab content_creation_assistant.ipynb
```

Use equivalent environment-variable commands on Windows. The environment file is an example only and is not loaded automatically. Dependencies are historical and unpinned; this is not a tested lockfile. Read the notebook before running it. API calls may spend credits or money on your own provider account.

## Security and verification

Hardcoded Google and Replicate credentials were replaced with environment variables. All notebook outputs and execution metadata were cleared. The original report and slides are excluded because an embedded screenshot in the report exposes credentials. Removing credentials here does not revoke them; rotate exposed keys in the provider accounts.

Do not treat this repository as a production-ready service.
