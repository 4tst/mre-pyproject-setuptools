# MRE for pyproject.toml with setuptools

## steps to reproduce

1. `clone the repo`
2. `uv sync`
3. `uv run main.py` or `uv run pytest`

### case not work

```toml
[tool.setuptools.packages.find]
where = ["src"]
include = ["sdk", "sdk*", "mylib", "mylib*"]
```

### case work

```toml
[tool.setuptools]
packages = ["mylib"]
```
