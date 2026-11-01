 **DAXD: Adaptive Agentic Honeypot Framework**

An agentic cybersecurity deception framework built with **LangGraph** and evaluated across open-weights Large Language Models. DAXD simulates dynamic SSH shell environments to engage threat actors, maintain multi-turn interaction state, and evaluate deception effectiveness.


## Architecture Overview
- **Deceptive Shell Agent:** Generates context-aware terminal output to simulate authentic Linux shell responses.
- **State & Memory Management:** Tracks interactive machine states across multi-turn attacker sessions (`graph.py`, `graph_hybrid.py`, `database.py`).
- **Automated LLM Judge Benchmark:** Evaluates terminal output fidelity, grounding, and attack tactic explanations against MITRE ATT&CK standards (`llm_judge_eval.py`, `run_benchmark.py`).

## Repository Structure
- `app.py` — Web interface and honeypot demo application.
- `graph.py` / `graph_hybrid.py` — Core LangGraph state flow implementations.
- `database.py` — Session storage and interaction state logging.
- `llm_judge_eval.py` — Automated LLM evaluation pipeline for scoring honeypot behavior.
- `judge_results_*/` — Benchmark evaluation runs and scoring datasets across models (DeepSeek-R1, Gemma 2, Mistral NeMo).
- `session_logs/` — Trace logs of simulated multi-turn attacker sessions.

##  Setup & Execution

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Poojitha004/DAXD-Deception-Framework.git](https://github.com/Poojitha004/DAXD-Deception-Framework.git)
   cd DAXD-Deception-Framework

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt

 3. **Configure environment:**
   Create and update your `.env` file with required model credentials.

4. **Launch the application:**
   ```bash
   python app.py

