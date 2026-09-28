# llm-frontdoor

FastAPI gateway in front of an LLM with response caching

Side project, maintained when I have time.

## What it does

- Provider SDK plugs into one function
- POST /v1/chat with prompt/model/max_tokens
- Latency measured and returned per request
- SHA-256 keyed in-memory response cache

## Examples

```bash
curl localhost:8000/v1/chat \
  -H 'content-type: application/json' \
  -d '{"prompt": "hello", "model": "gpt-4o-mini"}'
```

## Install

```bash
pip install -r requirements.txt
uvicorn main:app --reload
```

## Project structure

```text
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── main.py
└── requirements.txt
```

## Acknowledgments

- README structure inspired by popular OSS templates
- Thanks to everyone opening issues with ideas

## License

MIT - see [LICENSE](LICENSE).
