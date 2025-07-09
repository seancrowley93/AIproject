# HANA Log Summarizer 🤖📊

A tiny command-line tool that parses SAP HANA trace (`.trc`) files, converts each
line into structured JSON, and (in later sprints) feeds that data to a
Generative-AI service so Basis and Ops teams can ask questions like:

> “Summarise today’s WARN and ERROR entries for the LogBackup component.”

---

## 🚀 Roadmap (90-day sprints)

| Sprint | Deliverable | Status |
|--------|-------------|--------|
| **1–2** | CLI parser ➜ JSON (this repo) | 🔄 in progress |
| **3–4** | Docker image + CI/CD | ⬜ |
| **5–6** | Kubernetes deploy + Prometheus metrics | ⬜ |
| **7–8** | LLM summariser via SAP Generative AI Hub | ⬜ |
| **9–12** | Teams bot + blog post | ⬜ |

---

## v0 JSON schema (“Sensible Default”)

```json
{
  "timestamp":  "2025-06-21 09:17:18.256148",
  "severity":   "INFO | WARN | ERROR",
  "component":  "LogBackup",
  "message":    "Error writing backup file: rc=258"
}
