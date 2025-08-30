# study-plan
This project is all about learning &amp; doing hands-on with a specific goal &amp; tasks

# Go-MCP Agents 🚀

This repository is a **5-day learning journey in Go** culminating in a **backend system that interacts with an MCP server (A2A protocol), streams data into a vector database, and leverages LLMs for semantic analysis**.

---

## 📌 Project Goals
1. Learn **Go programming language** (from basics → concurrency → networking).
2. Build an **MCP-compatible backend** that can register and route **agents**.
3. Implement a **streaming engine** in Go to feed embeddings into a **vector database**.
4. Integrate an **LLM** to perform semantic analysis and guide **agent selection**.
5. Deliver a **demo project**: semantic classification & entity extraction pipeline.

---

## 🏗️ System Architecture

```mermaid
flowchart TD
    User[User Input] --> Backend[Go Backend Server]
    Backend --> MCP["MCP Server (A2A Protocol)"]
    MCP --> AgentA[Agent A: Classifier]
    MCP --> AgentB[Agent B: Entity Extractor]
    Backend --> Stream[Streaming Engine]
    Stream --> VectorDB[(Qdrant Vector DB)]
    Backend --> LLM["LLM: OpenAI GPT-4o / Claude / Ollama"]
    VectorDB --> LLM
    LLM --> Backend
    Backend --> User


