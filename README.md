# ErrorxHosting

Premium dark-crimson Python project hosting panel built with Flask.

## Features
- User accounts and admin panel (existing project functionality retained)
- Multi-file upload and ZIP project import with folder structure
- Python, HTML, CSS, JavaScript, JSON, YAML, TOML, Markdown, SQL, CSV, XML and common image assets
- Optional `requirements.txt` installation
- Startup file selection and process controls
- Per-user project directories and logs

## Run locally
```bash
pip install -r requirements.txt
python app.py
```

Set a strong `SECRET_KEY` environment variable before deployment. This application runs uploaded Python code as processes. Only deploy it in an isolated environment with OS/container resource limits, network restrictions, per-user quotas, and a non-root service account. Do not expose untrusted user code execution directly to the public internet without sandboxing.

ZIP uploads are checked for path traversal and symlinks. Allowed file types are explicitly limited in `app.py`.
