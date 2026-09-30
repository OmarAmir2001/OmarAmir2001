# Hi, I'm Omar Amir 👋

**AI Engineer · Giza, Egypt**

I build LLM agents that know when they're wrong. My work is agentic RAG systems in production: retrieval you can trace, answers checked by separate judges, a human stepping in when the model isn't sure, and the monitoring you need to trust all of it.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-omar--amir-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/omar-amir-556746220)
[![Email](https://img.shields.io/badge/Email-omaramir2001%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:omaramir2001@gmail.com)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-OmarAmir2001-FFD21E?logo=huggingface&logoColor=black)](https://huggingface.co/OmarAmir2001)

---

## 🚀 Featured projects

### 🎧 [Handbook Assistant: Customer Support Agent](https://github.com/OmarAmir2001/Customer_Support)

[![CI](https://github.com/OmarAmir2001/Customer_Support/actions/workflows/ci.yml/badge.svg)](https://github.com/OmarAmir2001/Customer_Support/actions/workflows/ci.yml)

A support agent that answers student questions from the CS and IS department handbooks. When it can't answer confidently, it **escalates to a human advisor instead of guessing**. It also learns from the questions advisors resolve.

- **Three separate LLM-judge gates** (context relevance, faithfulness, answer relevance) decide when to escalate. The model is never asked to rate its own confidence. The judges **fail closed**: if a judge breaks, the question goes to a human.
- **Tickets that survive a restart.** Escalating ends the agent run. The advisor answers hours later, and the answer goes back into the same conversation via `thread_id`. The ticket flow (`pending → under_review → resolved / rejected / closed / reopened`) has an audit trail and handles two advisors acting at once.
- **A learning loop an advisor controls.** Resolved answers join the knowledge base only when an advisor chooses to add them. Handbook text always ranks first, and an answer that contradicts the handbook is held back for review.
- **Built like a production service.** FastAPI, async SQLAlchemy, Alembic, Postgres and pgvector, Docker Compose, nginx, structlog with correlation IDs, and Prometheus and Grafana with custom metrics and 7 alert rules. **115 tests in CI.**

`LangGraph` `FastAPI` `pgvector` `PostgreSQL` `Groq` `Cohere` `Prometheus` `Grafana` `Docker` `uv`

---

### ⚖️ [Mizan: Egyptian Labor Law Assistant](https://github.com/OmarAmir2001/mizan)

🔗 **[Live demo on Hugging Face Spaces](https://huggingface.co/spaces/OmarAmir2001/mizan)**

Mizan (ميزان, "balance" in Arabic) is a legal assistant that answers questions about Egyptian labor law in **Arabic and English**, and cites the articles it used.

- **Corrective RAG loop.** It grades each retrieved chunk. If retrieval was poor, it rewrites the question into more precise legal wording and searches again, so answers are built only from relevant legal text.
- **Arabic and English search** with `multilingual-e5-large` embeddings and automatic language detection.
- **Memory across sessions.** Using LangGraph Store and Trustcall, it remembers each user's name, profession and preferences, and updates its own instructions for that user from their feedback.
- Streams answers token by token, works with LangGraph Studio, and runs on Hugging Face Spaces.

`LangGraph` `Groq · Llama 3.3 70B` `ChromaDB` `Sentence-Transformers` `Trustcall` `Gradio`

---

### 🏛️ Visioneer: graduation project

An Android app for creating and visualizing floor plans. With a colleague, I **fine-tuned Stable Diffusion v1.5 twice using Hugging Face PEFT**: once for schematic designs without furniture, and once for furnished layouts, trained on a modified *pseudo-floor-plan-12k* dataset.

`Stable Diffusion` `PEFT` `Hugging Face` `PyTorch`

---

## 🛠️ Tech stack

- **LLM & agents:** LangGraph · LangChain · RAG / CRAG · LLM-as-judge · Trustcall · Groq · Cohere · Hugging Face
- **Backend:** Python · FastAPI · Pydantic v2 · SQLAlchemy 2 (async) · Alembic · Gradio
- **Data & vectors:** PostgreSQL · pgvector · ChromaDB · Qdrant
- **MLOps & infra:** Docker Compose · nginx · Prometheus · Grafana · structlog · GitHub Actions · pytest · Locust · uv
- **ML / DL:** PyTorch · TensorFlow · Keras · scikit-learn · NumPy · Pandas

---

## 🎓 Background

- **B.Sc. Computer Science & Software Engineering**, Culture and Science City (2020–2024), graduated with honors
- **Certificates:** Deep Learning Specialization · Machine Learning Specialization · Mathematics for ML & Data Science · Data Analyst with Python
- **Languages:** Arabic (native) · English (full professional) · German (professional working)

---

<p align="center"><i>Open to AI / ML engineering roles. Get in touch on <a href="https://www.linkedin.com/in/omar-amir-556746220">LinkedIn</a> or by <a href="mailto:omaramir2001@gmail.com">email</a>.</i></p>
