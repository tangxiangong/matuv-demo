# Maturin uv
```bash
uv init --build-backend maturin matuv-demo
cd matuv-demo
mkdir python
mv src/matuv_demo python/
# edit pyproject.toml ...
uv sync
source .venv/bin/activate
maturin build
```
## pyproject.toml
```toml
[tool.maturin]
features = ["pyo3/extension-module"]
module-name = "matuv_demo._core"
python-source = "python"
```


