# FastAPI Template

A simple FastAPI template using [uv](https://docs.astral.sh/uv/) for fast Python package management.

## Features

- 🚀 FastAPI web framework
- ⚡ uv for fast dependency management
- 🐳 Docker support
- 🎯 Python 3.12

## Quick Start

### Prerequisites

- [uv](https://docs.astral.sh/uv/getting-started/installation/) installed
- Python 3.12 (managed by uv)

### Development

1. Clone the repository:
```bash
git clone git@github.com:Bocampagni/fastapi-template.git
cd fastapi-template
```

2. Install dependencies:
```bash
uv sync
```

3. Run the development server:
```bash
uv run fastapi dev app/main.py
```

The API will be available at:
- App: http://localhost:8000
- Interactive docs: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

### Docker

Build and run with Docker:

```bash
docker build -t fastapi-template .
docker run -p 80:80 fastapi-template
```

## API Endpoints

- `GET /` - Hello World
- `GET /items/{item_id}` - Get item by ID with optional query parameter

## Project Structure

```
.
├── app/
│   ├── __init__.py
│   └── main.py          # FastAPI application
├── dockerfile           # Docker configuration
├── pyproject.toml      # Project dependencies
├── uv.lock            # Dependency lock file
└── README.md
```

## Adding Dependencies

```bash
# Add a new dependency
uv add package-name

# Add a development dependency
uv add --dev package-name
```