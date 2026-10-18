<!-- ============ HEADER ============ -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,100:2F81F7&height=200&section=header&text=Shashank%20Pratap%20Singh&fontSize=42&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Python%20%7C%20Backend%20%7C%20Django&descAlignY=58&descSize=18" width="100%" />

<a href="https://github.com/ShashankSingh2020"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=700&lines=Backend+developer+building+multi-tenant+systems;Django+%7C+DRF+%7C+PostgreSQL+%7C+Celery+%7C+Redis;RAG+with+pgvector+%26+Gemini;300%2B+LeetCode+problems+solved+in+C%2B%2B" alt="Typing SVG" /></a>

<br/>

<a href="https://www.linkedin.com/in/shashank-pratap-singh-530437303/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:singh2020shashank@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://leetcode.com/u/Shashank_pratap_singh/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" /></a>
<a href="YOUR-RESUME-LINK"><img src="https://img.shields.io/badge/Resume-111111?style=for-the-badge&logo=readthedocs&logoColor=white" /></a>

</div>

---

## 👨‍💻 About Me

I'm an **Electronics & Communication Engineering** student at **Bangalore Institute of Technology** (CGPA **8.78**) who builds backend systems. I moved from core electronics into software because I enjoy solving problems that live in the data layer: tenant isolation, concurrency, background jobs, and clean APIs.

My three main projects share one theme: **designing multi-tenant systems that stay correct under real-world constraints**, from isolating vector embeddings per organization to making a ledger append-only at the model layer. I back this up with regular **DSA practice in C++** (333 LeetCode problems solved) and solid fundamentals in **DBMS, OOP and Computer Networks**.

> 🎯 **Open to:** Entry-level **Python Developer**, **Backend Engineer** and **SDE** roles, and internships.

---

## 🚀 Featured Projects

### 🧠 [Multi-Tenant Enterprise AI Knowledge Engine (RAG)](https://github.com/ShashankSingh2020/multi-tenant-rag-engine)
A multi-tenant Retrieval-Augmented Generation SaaS where each organization searches its own private documents with AI, with no cross-tenant data leakage.

- **Tenant isolation:** `Organization → Project → Document → DocumentChunk` hierarchy; vector searches are pre-filtered by project and organization membership *before* similarity ranking.
- **Async ingestion:** uploads return `201 Created` with `PENDING` status while **Celery + Redis** workers extract text, chunk (300-word window, 30-word overlap) and generate embeddings.
- **Concurrency-safe metering:** per-organization token and request quotas using `select_for_update()` and `F()` expressions, returning `429` when limits are hit.
- **Vector search:** PostgreSQL **pgvector** with 768-dim embeddings, **Gemini 2.5 Flash** for answers, with cited source chunks.
- **Audit trail and docs:** audit logging for ingestion, auth and AI queries, plus OpenAPI/Swagger docs.
- **Stack:** `Django` `DRF` `PostgreSQL` `pgvector` `Celery` `Redis` `Gemini` `Streamlit` `Docker` `pytest`
- 🔗 [Live app](https://multi-tenant-rag-engine.streamlit.app) · [API docs](https://multi-tenant-rag-engine.onrender.com/api/docs/) · 💻 [Source](https://github.com/ShashankSingh2020/multi-tenant-rag-engine)

---

### 🎫 [Enterprise Intelligent Support Ticket System](https://github.com/ShashankSingh2020/support-ticket-system)
A production-style support ticket backend with role-based access, SLA monitoring and AI-assisted ticket classification.

- **Access control:** custom email-based user model with four roles (`ADMIN`, `MANAGER`, `AGENT`, `CUSTOMER`) enforced by server-side DRF permissions.
- **Workflow and audit:** state-machine status transitions with an immutable `TicketEvent` log on every action.
- **Async processing:** Celery + Redis, using `transaction.on_commit` hooks so tasks are dispatched only after the database commit.
- **AI classification:** dual-mode engine, a deterministic local mock (no API key needed) and a production **Gemini** integration.
- **API quality:** OpenAPI 3.0 docs via `drf-spectacular` and rate-limited endpoints.
- **Stack:** `Django 5` `DRF` `Celery` `Redis` `Gemini` `Docker` `pytest`
- 💻 [Source](https://github.com/ShashankSingh2020/support-ticket-system)

---

### 📦 [Multi-Tenant E-Commerce Inventory Ledger](https://github.com/ShashankSingh2020/multi-tenant-inventory-ledger)
A retail platform that provisions fully isolated store workspaces for different vendors from a single PostgreSQL database.

- **Subdomain routing:** middleware resolves the tenant from the request host (for example `puma.localhost:8000`).
- **Automatic scoping:** the active tenant is bound to the request thread with `threading.local()`, and a custom manager appends `WHERE tenant_id = X` to every query, so even a plain `Product.objects.all()` stays isolated.
- **Append-only ledger:** the `LedgerEntry` double-entry log rejects modification of past records.
- **Cross-tenant guards:** model validation checks foreign-key tenant matches before writes.
- **Stack:** `Django` `PostgreSQL` `HTMX` `Tailwind CSS`
- 💻 [Source](https://github.com/ShashankSingh2020/multi-tenant-inventory-ledger)

---

## 🛠️ Tech Stack

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

### Backend & Databases
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/Django_REST_Framework-A30000?style=for-the-badge&logo=django&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI-6BA539?style=for-the-badge&logo=openapiinitiative&logoColor=white)

### AI / GenAI
![Gemini](https://img.shields.io/badge/Google_Gemini-4E86F7?style=for-the-badge&logo=google&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
**RAG · Embeddings · Vector Search**

### Frontend
![HTMX](https://img.shields.io/badge/HTMX-3366CC?style=for-the-badge&logo=htmx&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

### DevOps, Cloud & Tools
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)

---

## 🏗️ Engineering Concepts I've Applied

| Concept | Where I used it |
|---|---|
| **Multi-tenancy** (row-level isolation, scoped querysets) | Inventory Ledger, RAG Engine |
| **Race-condition prevention** (`select_for_update`, `F()` expressions) | RAG Engine quota metering |
| **Async task queues** (Celery, Redis, `transaction.on_commit`) | RAG Engine, Support Ticket System |
| **Vector search** (pgvector, embeddings, RAG pipeline) | RAG Engine |
| **Role-based access control** | Support Ticket System, RAG Engine |
| **Immutable audit logs / append-only ledgers** | All three projects |
| **API design** (JWT auth, throttling, OpenAPI docs) | RAG Engine, Support Ticket System |
| **Containerization** (Docker, docker-compose) | RAG Engine, Support Ticket System |

---

## 🧠 DSA & Problem Solving

<div align="center">

[![LeetCode](https://img.shields.io/badge/LeetCode-333_problems_solved-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Shashank_pratap_singh/)
![Language](https://img.shields.io/badge/Language-C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Striver](https://img.shields.io/badge/Striver's_A2Z_Sheet-~80%25-success?style=for-the-badge)

</div>

- 🏅 **LeetCode badges:** 50 Days Badge 2025, 50 Days Badge 2026 and 100 Days Badge 2026
- 💪 **Strongest topics by problems solved:** Arrays (173+), Strings (69+), Dynamic Programming (63+), Hash Tables (63+), Trees (45+), Backtracking (20+)
- 🎯 Practicing in C++ for online assessments and technical interviews

---

## 📊 Skills at a Glance

| Area | What I work with | Level |
|---|---|---|
| **Backend** | Django, DRF, REST API design, JWT auth, Celery | Comfortable building full apps |
| **Databases** | PostgreSQL, pgvector, SQL, schema design, DBMS concepts | Comfortable |
| **AI / GenAI** | Gemini API, embeddings, RAG pipeline, LangChain | Applied in a project, still growing |
| **DSA** | C++, 333 LeetCode problems, ~80% of Striver's A2Z sheet | Strong and improving |
| **CS Fundamentals** | OOP, DBMS, Computer Networks | Solid, networks in progress |
| **DevOps / Cloud** | Docker, Redis, AWS basics, Git, deployment on Render and Vercel | Foundational |

---

## 📚 Learning Journey

<details>
<summary><b>✅ Completed</b></summary>

- OOP, DBMS, SQL and PostgreSQL fundamentals
- Python and C++ programming
- Django and Django REST Framework
- Docker, AWS and Redis (course playlists with hands-on practice)
- Generative AI with LangChain (covering RAG)

</details>

<details>
<summary><b>🔄 In progress</b></summary>

- Computer Networks
- Data Structures & Algorithms (Striver's A2Z sheet and LeetCode)

</details>

<details>
<summary><b>🎯 Next up</b></summary>

- Add CI/CD (GitHub Actions) to my backend projects
- Deploy a Dockerized Django app on AWS
- Deeper work on caching and performance with Redis

</details>

---

## 🎓 Education

| Qualification | Institution | Score |
|---|---|---|
| B.Tech, Electronics & Communication Engineering | Bangalore Institute of Technology | CGPA 8.78 |
| Class XII | St. Patrick's Senior Secondary School, Jaunpur | 86% |
| Class X | St. Patrick's Senior Secondary School, Jaunpur | 86% |

---

## 🏆 Achievements & Community

- 🧩 **333 LeetCode problems** solved in C++ with 100-day streak badge (2026)
- 🦈 **Pull Shark** GitHub achievement
- 🎃 Contributed to **GDSC BIT's Hacktoberfest 2023** repositories

---

## 📈 GitHub Stats

<!-- Enable this block once you have a few more weeks of regular commits, so the numbers look good -->
<!--
<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=ShashankSingh2020&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ShashankSingh2020&layout=compact&theme=tokyonight&hide_border=true" />
</p>
-->

---

## 💬 Ask Me About

- Designing multi-tenant architectures in Django
- Building a RAG pipeline with pgvector and Gemini
- Preventing race conditions with PostgreSQL row-level locks
- How I prepare for DSA rounds in C++
- Moving from an ECE background into software

---

## 📫 Let's Connect

I'm actively looking for **entry-level Python / Backend / SDE** opportunities. If you have an opening or want to talk about a project, reach out:

- 📧 **Email:** [singh2020shashank@gmail.com](mailto:singh2020shashank@gmail.com)
- 💼 **LinkedIn:** [shashank-pratap-singh](https://www.linkedin.com/in/shashank-pratap-singh-530437303/)
- 🧩 **LeetCode:** [Shashank_pratap_singh](https://leetcode.com/u/Shashank_pratap_singh/)
- 📄 **Resume:** [Download](YOUR-RESUME-LINK)

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2F81F7,100:0D1117&height=120&section=footer" width="100%" />

</div>
