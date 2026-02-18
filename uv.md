# ⚡ UV — Modern Python Package Manager (README)

> **A fast, reliable replacement for pip — built for modern Python projects.**

This guide explains how to use **uv** with Python virtual environments to solve common installation issues, dependency conflicts, and slow builds.

---

## 🚀 What is uv?

**uv** is a modern Python package manager written in Rust.  
It replaces `pip`, `pip-tools`, and `virtualenv` with a **single, extremely fast tool**.

### Why uv exists:
- pip installs are slow
- dependency resolution fails often
- large projects break easily
- AI / ML environments are painful to reproduce

**uv fixes all of this.**

---

## ✨ Key Benefits of uv

- ⚡ **10–100x faster than pip**
- 🧠 **Reliable dependency resolution**
- 🔒 **Reproducible environments**
- 🤖 **Perfect for AI / ML projects**
- 🧼 **Clean, modern workflow**
- 🛠️ **Drop-in replacement for pip**

---

## 📦 Install uv

### Windows (PowerShell)
```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

### macOS / Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Verify installation:
```bash
uv --version
```

---

## 🧪 Create a Virtual Environment (Recommended)

```bash
uv venv .venv
```

Activate it:

**Windows**
```bash
.venv\Scripts\activate
```

**macOS / Linux**
```bash
source .venv/bin/activate
```

---

## 📥 Install Packages with uv

Install a single package:
```bash
uv pip install requests
```

Install from requirements file:
```bash
uv pip install -r requirements.txt
```

Install editable project:
```bash
uv pip install -e .
```

---

## 🔒 Lock Dependencies (Reproducible Builds)

Generate lock file:
```bash
uv pip freeze > requirements.lock
```

Reinstall exactly:
```bash
uv pip install -r requirements.lock
```

---

## ⚔️ pip vs uv (Quick Comparison)

| Feature | pip | uv |
|------|----|----|
| Speed | Slow | ⚡ Very Fast |
| Resolver | Weak | Strong |
| Locking | Manual | Easy |
| AI / ML | Painful | Smooth |
| Modern Python | ❌ | ✅ |

---

## 🤖 AI / ML Example

```bash
uv pip install numpy pandas scikit-learn torch transformers
```

---

## 🧑‍💼 Best Practices

- Use **uv + venv** together
- Lock dependencies for teams
- Commit lock files
- One environment per project
- Avoid global installs

---

## 🌟 Final Thought

> **pip was built for the past.  
> uv is built for the future of Python.**
