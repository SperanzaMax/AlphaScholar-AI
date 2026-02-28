# AlphaScholar-AI: The Autonomous Zero-Cost Research Engine

**AlphaScholar** is an elite, fully autonomous AI research agent designed for the [OpenClaw framework](https://github.com/npx-clawhub). 
It triangulates scientific data (PubMed/arXiv) and delegates the heavy lifting of reading PDFs/abstracts to a swarm of unpaid "intern" models running completely virtually and asynchronously, while the primary "Director" model orchestrates the flow and synthesizes the knowledge. 

The ultimate goal? **High-speed, comprehensive, zero-token-cost literature reviews.** 

##  The Origin Story: A True AI Hive-Mind Collaboration

This skill wasn't built by a human alone. It was designed, engineered, and optimized by a unique collaborative effort between **Maxi** (Human "Principal Investigator" & OpenClaw Architect) and an elite council of LLMs!

 **Credits & Contributions:**
*   **Maxi (Creator & Orchestrator):**. The architectural vision of the "Director vs. Interns" layout, and established the ruthless logic of zero-token-spend for heavy academic reading.
*   **Claude:** Contributed the **Armor & Architecture**. It built the flawless defensive programming structure, the `TokenBudget` tracker, explicit typing, and anti-prompt-injection mechanisms.
*   **DeepSeek:** Contributed the **Speed**. It pointed out that sequential paper processing was too slow and rewrote the dispatch logic using `asyncio` and `ThreadPoolExecutors` for concurrent execution.
*   **OpenAI (ChatGPT):** Suggested the core structure for the `delegate_to_intern` system and JSON schema validation.
*   **Grock:** Suggested adopting `BioPython` and refined the data extraction pipelines specifically for Biochemistry (like the 33-mer celiac peptide).
*   **Gemini:** Structured the README, documented the repository, and handled the GitHub integration process for Maxi.
*   **Qwen & Kimi:** Assisted in earlier brainstorming for the 50-Skill Roadmap that paved the way for AlphaScholar.

Together, we've created the ** Elite Agentic Skills**. 

## Features

*   **Concurrency Swarm (DeepSeek inspired):** Sends up to 8 "Intern" subagents to read different papers in parallel via thread execution, turning a 5-minute linear task into a 30-second burst.
*   **Token Budgeting & Security (Claude inspired):** Sanitizes inputs, enforces strict RAG collection names, and calculates exactly how many thousands of tokens you just saved by forcing small, free agents to do the grunt work.
*   **PubMed/arXiv RAG Injection:** Auto-vectors findings straight into `brain_engine.py`.

## Installation

1.  Clone this repository into your OpenClaw skills workspace:
    ```bash
    cd ~/.openclaw/workspace/skills/
    git clone https://github.com/[YOUR_USERNAME]/AlphaScholar-AI.git
    mv AlphaScholar-AI scientific_research_optimizer
    ```
2.  Install dependencies in your active virtual environment:
    ```bash
    pip install httpx tiktoken pydantic
    ```
3.  Ensure your `openclaw.json` has an intern named, e.g., `becario-trinity` running on a free OpenRouter model.

## Open Source Note
Feel free to fork and extend. If you like the idea of multiple LLMs collaborating to build an Agentic Framework, give us a Star!
