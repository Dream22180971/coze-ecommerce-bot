<div align="center">

# Coze Ecommerce Support Bot

**Build a knowledge-base-powered ecommerce support bot with Coze without writing application code.**

[English](./README.md) | [简体中文](./README.zh-CN.md)

[![Coze](https://img.shields.io/badge/Coze-Platform-7C3AED?style=for-the-badge)](https://www.coze.cn/)
[![Knowledge Base](https://img.shields.io/badge/RAG-Knowledge+Base-2563EB?style=for-the-badge)](#-knowledge-base)
[![No Code](https://img.shields.io/badge/BUILD-No--Code-111827?style=for-the-badge)](#-quick-start)
[![License](https://img.shields.io/badge/LICENSE-MIT-10B981?style=for-the-badge)](./LICENSE)

</div>

---

## 🎯 What it is

A platform-based ecommerce support bot built with Coze, a prompt, and a small knowledge base.

The repository focuses on a simple use case: repetitive customer questions such as returns, logistics and payment.

---

## 🎬 Demo

<div align="center">

<img width="88%" alt="Coze ecommerce support bot" src="https://github.com/user-attachments/assets/a2f91b7e-4569-4f06-9efd-503a5479d81c" />

<img width="88%" alt="Coze knowledge workflow" src="https://github.com/user-attachments/assets/d1a82829-c5bb-4c62-912a-c8aaec0cecf1" />

</div>

---

## ⚡ Quick Start

This project is configured in Coze rather than built locally.

1. Create or import a bot in Coze.
2. Upload the Markdown files from `knowledge/`.
3. Wait for the platform to chunk and index the documents.
4. Connect the knowledge base to the bot / workflow.
5. Test representative customer questions.
6. Publish to the channel you need.

---

## 📚 Knowledge Base

The repository includes example policy content for common ecommerce support topics:

| Document area | Typical questions |
|---|---|
| FAQ | accounts, orders, payment, coupons, membership |
| Returns | eligibility, process, refund timing |
| Logistics | delivery time, shipping fee, tracking and exceptions |

---

## 🧪 Suggested Test Set

Do not validate the bot with only one happy-path question.

Test at least:

| Test | What to check |
|---|---|
| “How do I return an item?” | correct policy and steps |
| “How long does delivery take?” | correct logistics source |
| “What payment methods are supported?” | correct FAQ retrieval |
| unsupported question | does not invent a policy |
| ambiguous wording | asks or answers appropriately |
| conflicting documents | retrieval behavior remains understandable |

---

## 🧩 Architecture

```mermaid
flowchart TB
    U[Customer] --> B[Coze Bot]
    B --> P[Prompt / Persona]
    B --> R[Knowledge Retrieval]
    R --> K[(Markdown Knowledge Base)]
    B --> L[LLM]
    L --> A[Answer]
```

---

## 💡 What this project demonstrates

- low-code / no-code AI application building
- prompt design
- knowledge-base configuration
- basic RAG thinking
- scenario-based bot testing
- deployment through a managed agent platform

---

## ⚠️ Current Limitations

- behavior depends on Coze platform capabilities and configuration
- this repository does not contain a self-hosted backend
- live order / logistics queries require external API integrations
- production customer service still needs escalation and human handoff design

---

## 🗺 Roadmap

- [x] FAQ / return / logistics knowledge
- [x] customer-service prompt
- [x] Coze knowledge retrieval
- [ ] order-status API
- [ ] logistics API
- [ ] conversation memory
- [ ] human escalation
- [ ] evaluation dataset
- [ ] more support channels

---

## 📄 License

[MIT](./LICENSE)

<div align="center">

**Start with the repeated questions. Add automation only where the knowledge is reliable.**

</div>
