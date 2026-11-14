<h1 align="center">Shreyas Jagannath</h1>

<p align="center">
  Applied AI Engineer in London. I make AI coding agents cheaper to run and safer to trust.
</p>

<p align="center">
  <a href="https://shreyasjagannath.com"><img src="https://img.shields.io/badge/Portfolio-shreyasjagannath.com-0E6B4E?style=flat-square&logo=googlechrome&logoColor=white" /></a>
  &nbsp;
  <a href="https://linkedin.com/in/shreyasjagannath"><img src="https://img.shields.io/badge/LinkedIn-shreyasjagannath-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  &nbsp;
  <a href="mailto:shreyasjag@hotmail.com"><img src="https://img.shields.io/badge/Email-shreyasjag@hotmail.com-EA4335?style=flat-square&logo=minutemailer&logoColor=white" /></a>
  &nbsp;
  <a href="https://pypi.org/project/nexus-mcp-ci/"><img src="https://img.shields.io/pypi/v/nexus-mcp-ci?style=flat-square&label=nexus-mcp-ci&color=3775A9&logo=pypi&logoColor=white" /></a>
  &nbsp;
  <a href="https://pepy.tech/projects/nexus-mcp-ci"><img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fjaggernaut007.github.io%2Fnexus-mcp%2Fdownloads-badge.json&style=flat-square" /></a>
</p>

---

## About

I make AI coding agents cheaper to run and safer to trust. I work on three things: the context an agent reads, the evaluation that gates each change, and the controls on what the agent can do. I have 8+ years in software, from computer-vision research for ISRO's Chandrayaan rover to production agents, and an MSc in Artificial Intelligence (Distinction) from the University of Surrey.

Most recently I was a Senior AI Engineer at **Lendable**, an FCA-regulated lender. I modelled incident.io, Jira, Datadog, GitHub and Backstage data into governed Snowflake metrics, gave engineers governed data access through a scoped agent skill, worked on the **AI Hub** that shows how the engineering org uses AI, and cut developer workflow times by up to 10%.

Before that, at **Klyft**, I cut tokens on the heaviest agent messages 10x (~100k → ~10k) and made the core agent 3x faster (60s → 20s). At **Move By Vision**, a guard-rail and validation layer removed 100% of AI crash failures in alpha-stage testing, generation latency fell 55% (15s → 7s), and I ran a GDPR and EU AI Act compliance audit.

**Open to offers** for applied AI, context engineering and AI governance roles where I build and own a system inside one team, at product companies or consulting and services firms. London, hybrid or on-site.

**Work with me** ([three ways to start](https://shreyasjagannath.com/#work-with-me)):
- **Hiring teams:** tell me about the role through the [contact form](https://shreyasjagannath.com/#contact).
- **Startup teams:** ask for a free 30-minute review of how your team uses AI coding agents: context, cost per correct change, review load and governance. It is a conversation, with no charge.
- **Hosts and organisers:** podcasts, meetups and conferences. The [speaker kit](https://shreyasjagannath.com/speaking/) has talk topics, bios and a headshot.

---

## Nexus-MCP

**Your coding agent reads less code to find the right file.** [Nexus-MCP](https://github.com/jaggernaut007/Nexus-MCP) is a local MCP server for Claude Code, Codex, Cursor and any MCP client: hybrid code search (local embeddings plus BM25) and a code graph. No API keys, no cloud. Open source under the MIT licence.

- **95% fewer tokens** than Grep and Read to reach the right file (median, 10 open-source repos in 10 languages), and **9× faster** search.
- In live Claude Code runs on 11 repos, the cost per task was lower on 8 of 11, with **64 of 66 tasks correct** against 61 of 66.
- **Where it loses, published:** on redis/redis (C) and tokio-rs/tokio (Rust) it used more tokens on an older build. A rerun is pending. The same code varies by about 20% in cost between runs.
- 1,676 tests, 24 Architecture Decision Records. On PyPI and the official MCP Registry. [All numbers and raw runs](https://jaggernaut007.github.io/nexus-mcp/benchmarks.html).

```bash
uvx --python 3.12 nexus-mcp-ci setup   # finds your MCP clients and asks before it writes
uvx --python 3.12 nexus-mcp-ci eval    # free, offline check on your own repo, no LLM
```

---

## Projects

| Project | Description | Tech |
|---|---|---|
| [**Nexus-MCP**](https://github.com/jaggernaut007/Nexus-MCP) | Local code-intelligence MCP server: hybrid search and a call graph, so a coding agent finds the right file with 95% fewer tokens (median, 10 repos). 8 tools (5 by default), call graphs in 10 languages, search in 25+, about 90 MB idle | Python · ONNX Runtime · LanceDB · tree-sitter · rustworkx |
| [**Protash**](https://github.com/jaggernaut007/Protash) | Describe a business intent and get a deployed prototype back in under 5 minutes. Six agent stages, with QA and review agents that request fixes before anything reaches the screen. [Live demo](https://protash.shreyasjagannath.com) | Next.js · TypeScript · DeepSeek · GCP Cloud Run |
| **Agent Harness** *(private)* | Connects agents to live databases and APIs and builds validated dashboards. Every SQL path goes through one read-only guard by construction, and no response model can carry a credential back to the LLM. Hardened through adversarial review; 274 tests | Python · FastAPI · sqlglot · SSE |
| **CR8** *(private)* | 3-agent LangGraph pipeline that turns a university curriculum into study guides, narrated video and quizzes. A two-layer evaluation framework gates every output | LangGraph · FastAPI · React · Cloud Run |
| **JobScout** *(private)* | Daily pipeline that pulls ~30,000 jobs from 13 ATS platforms and checks each employer and salary against fixed rules. A free keyword tier removes ~80% of jobs before the LLM tier, so LLM cost stays under $0.01/day. 1,035 tests | Python · LangGraph · Embeddings |
| [**Health Intelligence Engine**](https://github.com/jaggernaut007/healthAgent) | Turns supplement queries into evidence-grounded recommendations from NIH DSLD and PubMed through a Neo4j knowledge graph. A Pharmacovigilance Critic checks each one against the user's allergies and medications | LangGraph · Neo4j · RAG · DeepEval |
| [**Knowledge Graph Agent**](https://github.com/jaggernaut007/fabric-context-portability) | Turns raw search history into a Neo4j knowledge graph, then generates personalised video with Gemini and Veo 3.1. 11 semantic categories extracted for under $1 in API cost | Python · Neo4j · Gemini · Veo 3.1 |
| [**RevGeni Agent**](https://github.com/jaggernaut007/RevGeniAgent) | Async multi-agent pipeline that crawls the web, qualifies companies, enriches contacts and writes leads into a GraphQL CRM | Python · Multi-agent · GCP · GraphQL |

---

## Skills

**AI & LLM Systems**

![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white&style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?logo=langchain&logoColor=white&style=flat-square)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-000000?style=flat-square)
![Google ADK](https://img.shields.io/badge/Google_ADK-4285F4?logo=google&logoColor=white&style=flat-square)
![MCP](https://img.shields.io/badge/MCP-000000?logo=modelcontextprotocol&logoColor=white&style=flat-square)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?logo=claude&logoColor=white&style=flat-square)
![DeepEval](https://img.shields.io/badge/DeepEval-5C6BC0?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-FF6F00?style=flat-square)

**LLM APIs**

![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?logo=openai&logoColor=white&style=flat-square)
![Gemini](https://img.shields.io/badge/Gemini_%2F_Vertex_AI-4285F4?logo=googlegemini&logoColor=white&style=flat-square)
![DeepSeek](https://img.shields.io/badge/DeepSeek_API-4D6BFE?style=flat-square)
![Anthropic](https://img.shields.io/badge/Claude_API-191919?logo=anthropic&logoColor=white&style=flat-square)

**ML**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white&style=flat-square)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white&style=flat-square)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?logo=huggingface&logoColor=black&style=flat-square)
![ONNX Runtime](https://img.shields.io/badge/ONNX_Runtime-005CED?logo=onnx&logoColor=white&style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white&style=flat-square)

**Languages & Frameworks**

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white&style=flat-square)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB&style=flat-square)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white&style=flat-square)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white&style=flat-square)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?logo=graphql&logoColor=white&style=flat-square)
![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white&style=flat-square)

**Data, Cloud & Infra**

![GCP](https://img.shields.io/badge/GCP-4285F4?logo=googlecloud&logoColor=white&style=flat-square)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?logo=snowflake&logoColor=white&style=flat-square)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?logo=googlebigquery&logoColor=white&style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white&style=flat-square)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?logo=neo4j&logoColor=white&style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=flat-square)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=white&style=flat-square)
![Argo CD](https://img.shields.io/badge/Argo_CD-EF7B4D?logo=argo&logoColor=white&style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white&style=flat-square)
![Datadog](https://img.shields.io/badge/Datadog-632CA6?logo=datadog&logoColor=white&style=flat-square)

---

## Experience

**Lendable Operations Ltd**
**Senior AI Engineer** · Jul 2026 – Sep 2026
- Modelled incident.io, Jira, Datadog, GitHub and Backstage data into governed, OKR-level Snowflake metrics that leadership could act on
- Gave engineers agentic access to governed data through a scoped, auditable agent skill rather than an MCP server, to meet FCA security requirements
- Worked on the AI Hub, a full-stack dashboard that unifies GitHub, Jira, Claude and Codex telemetry
- Cut developer workflow times by up to 10% by instrumenting the organisation's agent skills, with automatic ticket-to-skill detection
- Built a company-level cycle-time model on the GitHub GraphQL API that attributes each PR to a team from historical contribution share, with a manager-facing correction loop
- Shipped on Terraform/Terragrunt, GitHub Actions and Argo CD, with Okta SCIM/OIDC authentication

**We Are Human Agency AB (Move By Vision)**
**Consultant (Pro Bono)** · Dec 2025 – Jun 2026
- Took over a Flutter and GCP healthtech platform in critical-failure alpha
- Built a guard-rail and validation layer across the Vertex AI integrations that removed 100% of AI crash failures in alpha-stage testing
- Cut generation latency by 55% (15s → 7s) and ran a GDPR and EU AI Act compliance audit

**Klyft Technologies**
**Founding AI Engineer** · Sep 2025 – Nov 2025
- Took an eight-agent coaching platform to production on Google ADK and Vertex AI, with each agent scoped to its own data
- Cut tokens on the heaviest messages 10x (~100k → ~10k) by pre-summarising wearable data and scoping each agent's data access
- Evaluated Gemini 2.5 Flash against Pro on golden datasets to near-parity, so Pro never ran in production
- Made the core workout-calibration agent 3x faster (60s → 20s) with async Pub/Sub processing and OpenTelemetry tracing

**Scan and Sew Inc.**
**Chief Data Officer (Founding Team)** · Oct 2024 – Aug 2025
- Shipped a Designer AI Assistant (RAG over design documents) and a real-time manufacturing tracking platform
- Evaluated custom Gaussian Splatting against third-party APIs and chose the API, which saved months of development

<details>
<summary>Earlier roles</summary>

**AIMAGE Technologies** · Founder & CTO · Jan 2020 – Aug 2023
- Grew the team to 10 across engineering, product and design
- Built a custom vectoriser and a graph-based vector database for visual search, live on a retail client's storefront
- Built a virtual try-on engine (OpenCV, PyTorch, Unity3D) on AWS (Lambda, ECS, Neptune, DynamoDB, Kinesis)

**Mage Ventures** · Founder & Consultant (Part-time) · Oct 2019 – Mar 2021
- Implemented a cross-platform payment gateway for Walmart-owned PhonePe
- Built a computer-vision checkout engine for grocery retail

**Cellstrat Inc.** · AI Consultant (Contract, Founding Team) · Oct 2018 – Oct 2020
- Delivered AI/ML work for TVS Motors, Target, Airbus and Volvo in PyTorch, TensorFlow and Keras on AWS
- Delivered a workshop at ODSC on enterprise AI and deep learning to 100+ professionals

**EndGate Global** · Full Stack Engineer (Founding Team) · Jul 2017 – Jul 2018
- Built bulk food-delivery order workflows in Java, Spring, Hibernate and MySQL

**ISRO** · AI Researcher Intern · Nov 2016 – Apr 2017
- Researched mono-vision depth detection for the Chandrayaan moon rover

</details>

---

## Education

- **MSc, Artificial Intelligence** (Distinction), University of Surrey, United Kingdom *(2024)*
- **Master's in Computer Applications** (First Class), Christ University, India *(2017)*
- **Bachelor's in Computer Applications**, Bangalore University, India *(2013)*

**Certifications:** Claude Code in Action, Model Context Protocol, Agent Skills, Building with the Claude API (Anthropic) · LangGraph & LangSmith (LangChain Academy) · Deep Learning & Computer Vision (Stanford)

**Publication:** *Modern Machine Learning Approaches for Robotic Path Planning* (peer-reviewed journal)

---

<p align="center">
  <a href="https://shreyasjagannath.com">Portfolio</a> ·
  <a href="https://linkedin.com/in/shreyasjagannath">LinkedIn</a> ·
  <a href="mailto:shreyasjag@hotmail.com">Email</a>
</p>
