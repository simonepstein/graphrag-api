# GraphRAG API

This project provides a FastAPI-based server implementation for handling both global and local structured searches using GraphRAG.

## Installation

Clone the repository and install the required dependencies using the following commands:

```bash
git clone git@github.com:noworneverev/graphrag-api.git
cd graphrag-api
```

```bash
python -m venv venv
```

```bash
source venv/bin/activate # for Linux
venv\Scripts\activate # for Windows
```

```bash
pip install -r requirements.txt
```

## Usage

```
python api.py
```

Open http://127.0.0.1:8000/docs/ to see the API documentation.

You can also use the interface at [GraphRAG Visualizer](https://noworneverev.github.io/graphrag-visualizer/) to run queries against the server.

![search](static/image.png)

## API Endpoints

- `/search/global`: Perform a global search using GraphRAG.
- `/search/local`: Perform a local search using GraphRAG.
- `/status`: Check if the server is up and running.

## Deployment

If deploying to caprover, the artifacts directory must be mapped as a volume, and the parquet files should be copied into place on the host machine. This is because the parquet files are not in git, and hence not deployable via caprover deploy.

e.g. /app/artifacts mapped to /home/ubuntu/graphrag-api/artifacts/iwsr on the host machine.
