---
name: AlphaScholar-Research-Optimizer
display_name: AlphaScholar Elite Researcher
version: 1.0.0
author: SperanzaMax & The AI Hive-Mind (Claude, DeepSeek, ChatGPT, Qwen, Kimi, Grock, Gemini)
category: scientific_research
tags: ["pubmed", "arxiv", "rag", "delegation", "async", "token-optimization", "bioinformatics"]
description: |
  AlphaScholar is the ultimate zero-cost, high-speed autonomous research engine. 
  It triangulates scientific information from PubMed/arXiv, identifies heavy-reading tasks, 
  and dispatches a swarm of subagent "interns" in pure asynchronous parallel execution via ThreadPoolExecutor. 
  It indexes findings in Petter's RAG via brain_engine.py and delivers a technical Markdown report 
  with exact token-savings percentages. Engineered for the OpenClaw framework.
requires_venv: scientific_venv
---

# SKILL: AlphaScholar-Research-Optimizer

**Welcome to AlphaScholar, the ultimate token-stingy, ultra-fast research orchestrator.**

This skill represents the pinnacle of multi-LLM engineering. By combining the **flawless logic, safety, and token-cost validation of Claude** with the **blazing fast parallel asynchronous execution engine of DeepSeek**, AlphaScholar guarantees maximum scientific output with zero premium token leakage.

## Input / Output
- **Input**: text string (molecular sequence, query, etc.)
- **Output**: 
  - Complete Markdown technical report in `~/research/report_{query}.md`
  - Automatic ingestion to RAG
  - Confirmation of tokens saved for the Director's budget.

## Tool Schema
```json
{
  "tools": [
    {
      "name": "optimize_research",
      "description": "Main orchestrator. AlphaScholar decides what to delegate to the swarm of unpaid interns.",
      "parameters": {
        "type": "object",
        "properties": {
          "query": { "type": "string", "description": "Keyword or sequence to investigate" },
          "depth": { "type": "string", "enum": ["quick", "medium", "comprehensive"], "default": "medium" },
          "sources": { "type": "array", "items": { "type": "string", "enum": ["pubmed", "arxiv"] }, "default": ["pubmed", "arxiv"] }
        },
        "required": ["query"]
      }
    }
  ]
}
```
