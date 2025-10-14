# InterPLM: Discovering Interpretable Features in Protein Language Models via Sparse Autoencoders

## Environment set up with `uv`

The following steps will set up a reproducible Python environment using `uv`. This approach avoids dependency conflicts and works seamlessly on HPC clusters.

### 1. Install uv 
This will install a single static binary in your `$HOME/bin`:
```
curl -LsSf https://astral.sh/uv/install.sh | sh
```
### 2. Navigate to the repository
```
cd ~/InterPLM
```

### 3. Create a virtual environment
Creates an isolated environment inside the repository:
```
uv venv .venv
```

### 4. Activate venv
```
source .venv/bin/activate
```

### 5. Install dependencies
Synchronize and install all dependencies listed in `pyproject.toml`:
```
uv sync
```
   This automatically resolves and locks dependencies for reproducibility (`uv.lock` file).

## Updating the environment
Whenever you modify dependencies (add or update a package), run:
```
uv sync --upgrade
```

or to install a single new package:
```
uv add <package-name>
```