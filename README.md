<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=17&pause=1200&color=C77DFF&center=true&vCenter=true&width=750&lines=Hey+there!+I'm+Pushya+%F0%9F%91%8B;Software+Engineer+%C2%B7+Full-Stack+Developer+%C2%B7+AI+Enthusiast;Python+%C2%B7+Docker+%C2%B7+PostgreSQL+%C2%B7+Django+%C2%B7+GenAI;Building+scalable+systems+that+matter+%F0%9F%9A%80)](https://git.io/typing-svg)

</div>

---

### Hey there, I'm Pushya 👋

<img align="right" width="280" src="15129348743443180.jpg" alt="profile image"/>

I'm a developer who loves building things that are both functional and thoughtful. I work mostly on backend systems, AI pipelines, and full-stack applications — always trying to write code that's clean, well-tested, and actually useful.

Curious by nature, I'm always picking up something new — right now that's cloud infrastructure, LLM-powered systems, and distributed design patterns. I believe good engineering and good thinking go hand in hand. When I'm not at my keyboard, you'll probably find me deep in a K-drama, listening to music, running trades, or designing something for fun.

```yaml
name:       B. C. Pushya
location:   Bengaluru, India 🇮🇳
degree:     M.Tech, Computer Science Engineering — NHCE, VTU
currently:  Open to Software Engineering roles 🔍
interests:  K-pop 🎵  ·  Intraday trading 📊  ·  Gamified productivity 🎮
```

---

### 🎯 Current Focus

- 🧠 Deepening knowledge in **distributed systems** and **cloud infrastructure (AWS)**
- 🤖 Exploring **LLM fine-tuning**, **RAG pipelines**, and **GenAI engineering**
- 🌱 Working toward **IBM DevOps**, **IBM GenAI Engineering**, and **AWS Cloud Support Associate** certifications
- 💻 Building out my project portfolio with algorithmically interesting systems
- 📈 Practising **DSA** (graphs, DP, heaps) consistently on LeetCode

---

### 🛠️ Skills & Technologies

<div align="center">

**Core**

<img src="https://skillicons.dev/icons?i=python,docker,postgres&theme=light"/>

**Backend**

<img src="https://skillicons.dev/icons?i=django,flask,redis,fastapi&theme=light"/>

**AI / ML**

<img src="https://skillicons.dev/icons?i=tensorflow&theme=light"/>

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-c77dff?style=for-the-badge&logoColor=white)
![LLaMA 2](https://img.shields.io/badge/LLaMA_2-7b2ff7?style=for-the-badge&logo=meta&logoColor=white)
![Watson NLP](https://img.shields.io/badge/Watson_NLP-0062FF?style=for-the-badge&logo=ibm&logoColor=white)

**DevOps & Cloud**

<img src="https://skillicons.dev/icons?i=git,github,aws,linux&theme=light"/>

</div>

---

### 🚀 Projects I'm Excited to Share

<div align="center">

<a href="https://github.com/Pushya26/mini_search_engine">
  <img height="130" src="https://github-readme-stats.vercel.app/api/pin/?username=Pushya26&repo=mini_search_engine&theme=tokyonight&hide_border=true&bg_color=0d0d1a&title_color=ff9de2&icon_color=c77dff&text_color=e2e8f0&cache_seconds=1800"/>
</a>
<a href="https://github.com/Pushya26/flight_tracking_system">
  <img height="130" src="https://github-readme-stats.vercel.app/api/pin/?username=Pushya26&repo=flight_tracking_system&theme=tokyonight&hide_border=true&bg_color=0d0d1a&title_color=ff9de2&icon_color=c77dff&text_color=e2e8f0&cache_seconds=1800"/>
</a>

<a href="https://github.com/Pushya26/chat_with_pdf_streamlit_llama2-main">
  <img height="130" src="https://github-readme-stats.vercel.app/api/pin/?username=Pushya26&repo=chat_with_pdf_streamlit_llama2-main&theme=tokyonight&hide_border=true&bg_color=0d0d1a&title_color=ff9de2&icon_color=c77dff&text_color=e2e8f0&cache_seconds=1800"/>
</a>
<a href="https://github.com/Pushya26/Cognitive-Customer-Insights">
  <img height="130" src="https://github-readme-stats.vercel.app/api/pin/?username=Pushya26&repo=Cognitive-Customer-Insights&theme=tokyonight&hide_border=true&bg_color=0d0d1a&title_color=ff9de2&icon_color=c77dff&text_color=e2e8f0&cache_seconds=1800"/>
</a>

</div>

<br/>

**🔍 Mini Search Engine** &nbsp;·&nbsp; `Python` `FastAPI` `BM25` `PageRank` `Inverted Index`

A domain-specific search engine for research papers, built entirely from scratch — no Elasticsearch. Crawls real arXiv metadata, builds a hand-rolled inverted index with postings lists on disk, constructs a citation graph and runs power-iteration PageRank on it, then combines both signals into a hybrid ranker (`score = α·BM25 + β·PageRank`). Exposes a paginated `/search` REST API via FastAPI with a CLI for crawl, index, serve, and stats commands.

<br/>

**✈️ Flight Tracking System** &nbsp;·&nbsp; `Python` `FastAPI` `WebSocket` `React` `CesiumJS` `Docker`

A multi-threaded real-time flight tracking system with a 3D globe frontend. Ingestion runs through a bounded producer-consumer pipeline (`queue.Queue`, maxsize 10,000) into a thread-safe `AircraftStateStore` (RLock + snapshot-on-read), a `GridSpatialIndex` for O(1) insert and bounding-box queries, and a per-aircraft `PositionRingBuffer`. Background workers handle stale aircraft eviction (every 30s) and O(n²) CPA conflict detection with caching (every 15s). The FastAPI backend streams live state snapshots over WebSocket every 2s; the React + CesiumJS frontend renders aircraft on a 3D OSM globe with great-circle route arcs and real-time selection highlights.

<br/>

**🧠 Chat with PDF** &nbsp;·&nbsp; `Python` `LLaMA 2` `ChromaDB` `LangChain` `Streamlit`

A production-ready RAG chatbot that answers questions grounded strictly in uploaded documents (PDF, TXT, MD, DOCX). The pipeline runs: smart chunking → embedding → ChromaDB vector store → top-k retrieval with confidence scoring → LLaMA 2 generation with answer refusal when the context doesn't support a response. Delivers answers with inline citations (`[DocName, page X]`), targets end-to-end latency ≤ 3 seconds, and ships with a Streamlit web UI, a CLI, and a Python API for programmatic access.

<br/>

**📊 Cognitive Customer Insights** &nbsp;·&nbsp; `Python` `TensorFlow` `Watson NLP` `Flask` `Streamlit` `K-Means`

An end-to-end AI customer segmentation system that processes both numerical purchase data and unstructured text feedback. Uses an Autoencoder to compress and extract latent features, then applies K-Means clustering to identify distinct customer segments. Exposes real-time segment predictions via a Flask REST API and ships a Streamlit dashboard for business users to explore segments and derive marketing insights without writing code.

---

### 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Pushya26&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d0d1a&title_color=ff9de2&icon_color=c77dff&text_color=e2e8f0&include_all_commits=true&count_private=true&cache_seconds=1800" height="165"/>
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Pushya26&layout=donut&theme=tokyonight&hide_border=true&bg_color=0d0d1a&title_color=ff9de2&text_color=e2e8f0&cache_seconds=1800&hide=jupyter%20notebook" height="165"/>

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=Pushya26&theme=tokyonight&hide_border=true&background=0d0d1a&ring=ff9de2&fire=c77dff&currStreakLabel=ff9de2&sideLabels=c77dff&currStreakNum=ffffff&sideNums=ffffff&dates=e2e8f0" width="55%"/>

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Pushya26&theme=tokyo-night&hide_border=true&bg_color=0d0d1a&color=ff9de2&line=c77dff&point=ffffff&area=true&area_color=7b2ff7" width="95%"/>

</div>

---

### 🤝 Let's Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pushya-bc-27b40a24b)
[![GitHub](https://img.shields.io/badge/GitHub-%23181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Pushya26)
[![Gmail](https://img.shields.io/badge/Gmail-%23EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:chandrupushya@gmail.com)

<br/>

![Profile Views](https://komarev.com/ghpvc/?username=Pushya26&style=for-the-badge&color=c77dff&label=PROFILE+VIEWS)

<br/><br/>

*「 Clean code. Real impact. Shipped. 」*

</div>
