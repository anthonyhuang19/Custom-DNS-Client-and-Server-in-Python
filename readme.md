# 🚀 CDN Cache API — A Lightweight Caching Layer for Content Delivery
![](figure/figure.png)
Welcome to the **CDN Cache API** project! This repository contains a robust caching system designed to simulate key CDN caching behaviors — including TTL-based expiration, LRU eviction, and an HTTP API interface for cache management. Perfect for learning, testing, or extending to production-grade systems!

---

## 🗂️ Project Overview

This project aims to build a **Content Delivery Network (CDN) cache layer** that:

- Efficiently caches HTTP responses with **time-to-live (TTL)** management
- Supports **Least Recently Used (LRU)** eviction when cache reaches capacity
- Differentiates cache entries by HTTP method & request path
- Provides a **FastAPI**-based HTTP interface to interact with the cache
- Includes a simulated backend server to mimic origin responses for testing
- Comes with a comprehensive **pytest** suite to ensure stability and correctness

---

## 📁 Project Structure
```bash
.
├── app.py # FastAPI application exposing cache API endpoints
├── cache.py # Cache core logic: TTL, eviction, and key management
├── main_server.py # Simulated origin backend server for testing purposes
├── test.py # Automated tests with pytest covering cache and API behaviors
├── test.sh # Shell script to run tests easily
├── requirements.txt # Python dependencies required for the project
└── pycache/ # Python bytecode cache files (auto-generated)
```

---

## ⚙️ Setup & Installation

1. **Create and activate** a Python 3.9+ virtual environment (recommended):

   ```bash
   python3 -m venv env
   source env/bin/activate   # macOS/Linux
   .\env\Scripts\activate    # Windows

2. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
## 🚀 Running the Application
Launch the FastAPI app locally with hot reload support:

```bash
uvicorn main_server:server --port 8000
uvicorn app:app --port 8080
````
---
## 🧪 Running Tests
```bash
pytest test.py -v
./test.sh
````
---
## 📌 Key Features
- **TTL Cache:** Automatically expires cache entries after a configurable duration.
- **LRU Eviction:** When capacity is full, least recently used items are removed.
- **Multi-Method Support:** Cache keys include HTTP method to avoid collisions.
- **API Metadata:** Responses include cache hit status and cache keys for transparency.
- **Test-Driven:** Comprehensive automated tests to maintain code quality.
- **Modular Design:** Easily extend cache policies or API features.

---

If you want, I can also help add:

- Status badges (e.g., build, coverage)
- Example API documentation with sample requests/responses
- Docker support or deployment instructions

Just let me know!







