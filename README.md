# LangGraph MongoDB Demo

A demonstration of integration between LangGraph and MongoDB for creating AI agents.

## Prerequisites

- Python 3.12 or higher

## Environment Setup - Step by Step Guide

### 1. Verify Python Installation
Make sure you have Python 3.12 or higher installed:

```bash
python --version
```

If you don't have Python 3.12+, download it from [python.org](https://www.python.org/downloads/).

### 2. Install uv (package and virtual environment manager)

`uv` is a modern and fast tool for managing Python dependencies:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

After installation, restart your terminal or run:

```bash
source ~/.bashrc  # or ~/.zshrc depending on your shell
```

Verify the installation:

```bash
uv --version
```

### 3. Clone and navigate to the project

```bash
git clone https://github.com/Adotel15/langgraph-mongodb-demo.git
cd langgraph-mongodb-demo
```

### 4. Create a virtual environment with uv

```bash
uv venv
```

This will create a `.venv` directory in the project root.

### 5. Activate the virtual environment

```bash
source .venv/bin/activate
```

You should see `(.venv)` at the beginning of your prompt, indicating that the virtual environment is active.

### 6. Install project dependencies

```bash
uv pip install -e .
```

### 7. Register the Jupyter kernel

To be able to use the virtual environment in Jupyter notebooks:

```bash
python -m ipykernel install --user --name=langgraph-mongodb-demo --display-name="LangGraph MongoDB Demo"
```

### 8. Configure environment variables 

Create a `.env` file:

```bash
cp .env.example .env

touch .env
```

Edit the `.env` file with your configurations:

```
OPENAI_API_KEY=your_api_key_here
MONGODB_URI=mongodb://localhost:27017/your_database
```

### 9. Open and configure the Jupyter Notebook

1. **Option A - Using VS Code:**
   - Open the `notebooks/agent.ipynb` file in VS Code
   - When the notebook opens, click "Select Kernel" in the top right corner
   - Select "LangGraph MongoDB Demo" from the list of available kernels

2. **Option B - Using Jupyter Lab/Notebook:**
   ```bash
   jupyter lab notebooks/agent.ipynb
   ```
   - In the notebook, go to Kernel → Change Kernel → LangGraph MongoDB Demo

### 10. Verify the installation

In the first cell of the notebook, run:

```python
import langchain
import langgraph
import pymongo
print("✅ All dependencies imported successfully")
```

## Deactivate the virtual environment

When you're done working:

```bash
deactivate
```