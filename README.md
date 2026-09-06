# Multi-Agent Customer Support Automation

<p align="center">
  <img src="https://img.shields.io/badge/Python-100%25-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/CrewAI-Multi--Agent%20Workflow-7C3AED?style=for-the-badge" alt="CrewAI">
  <img src="https://img.shields.io/badge/Ollama-LLaMA%203.2-10B981?style=for-the-badge" alt="Ollama">
  <img src="https://img.shields.io/badge/Support%20Automation-AI%20Powered-0EA5E9?style=for-the-badge" alt="AI Powered">
</p>

<p align="center">
  <b>A multi-agent customer support system built with CrewAI and Ollama.</b><br>
  Support responses are drafted by one agent and reviewed by a QA agent for quality, accuracy, and consistency.
</p>

---

## Overview

**Multi-Agent Customer Support Automation** is a modular Python-based AI system designed to streamline customer support workflows.

It combines:
- a **Support Agent** that drafts helpful responses,
- a **QA Agent** that reviews and improves the response,
- **web scraping / documentation lookup** for grounded answers,
- and **Ollama (LLaMA 3.2)** for local or flexible model execution.

This project is built for teams and developers who want:
- faster support turnaround,
- better response quality,
- more consistent answers,
- and a workflow they can extend easily.

---

## Why this project?

- **Faster support resolution** through automation
- **Higher response quality** with a review step before sending
- **Documentation-backed answers** using scraped or retrieved sources
- **Flexible architecture** that can be extended with new agents or tools
- **Local-first AI support** with Ollama integration

---

## Key Features

- Multi-agent workflow inspired by CrewAI
- Support agent for response drafting
- QA agent for review and refinement
- Web scraping for documentation-backed replies
- Ollama integration with LLaMA 3.2
- Modular Python structure
- Easy to extend with more agents, tools, or knowledge sources
- Clear separation between research, drafting, and validation

---

## How It Works

1. **User submits a support question**
2. **Support Agent** generates an initial answer
3. **Documentation / web sources** are checked for supporting context
4. **QA Agent** reviews the draft for:
   - clarity
   - correctness
   - tone
   - completeness
5. **Final response** is returned

---

## Project Structure

```text
Multi-Agent-Customer-Support-Automation/
├── agents/
│   ├── support_agent.py
│   └── qa_agent.py
├── connectors/
│   ├── ollama_driver.py
│   └── web_search.py
├── orchestrator.py
├── run_pipeline.py
├── config/
│   └── config.yml
├── outputs/
│   └── articles/  (or generated responses)
└── README.md
```

> Note: Adjust the structure above to match your exact repository files if needed.

---

## Getting Started

### Prerequisites

- Python 3.8+
- pip or poetry
- Ollama installed locally
- Required API keys or connectors for external data sources, if used

### Installation

```bash
git clone https://github.com/Saqib-Agentic-AI/Multi-Agent-Customer-Support-Automation.git
cd Multi-Agent-Customer-Support-Automation
python -m venv .venv
```

#### Activate the virtual environment

**macOS / Linux**
```bash
source .venv/bin/activate
```

**Windows**
```bash
.venv\Scripts\activate
```

#### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Configuration

1. Copy the example config:
```bash
cp config/example_config.yml config/config.yml
```

2. Update model and agent settings:
   - Ollama model name
   - agent prompts
   - workflow options
   - external data sources

3. Add any required environment variables to a `.env` file.

---

## Usage

### Run the pipeline

```bash
python run_pipeline.py --topic "Customer refund policy clarification" --audience "support team"
```

### Interactive mode

```bash
python interactive_agent.py
```

### Expected output

- final drafted response
- QA-reviewed response
- optional logs or intermediate JSON
- saved output files for traceability

---

## Example Workflow

```text
Support Question
   ↓
Support Agent drafts response
   ↓
Documentation / web context retrieved
   ↓
QA Agent reviews response
   ↓
Final polished answer delivered
```

---

## Extending the System

You can extend the project by:

- adding more agents in the `agents/` directory
- swapping the model driver in `connectors/`
- adding new data sources or search connectors
- introducing extra QA checks
- exporting results to Markdown, HTML, PDF, or CMS platforms

---

## Best Practices

- Start with a small workflow before scaling up
- Keep prompts versioned and documented
- Log source URLs and timestamps for auditability
- Pin model versions when reproducibility matters
- Review QA feedback to improve agent instructions

---

## Contributing

Contributions are welcome.

If you’d like to contribute:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request
4. Include tests and a clear description of changes

---

## Support

For bugs, ideas, or feature requests, please open an issue.

---

## Credits

Built with:
- **CrewAI**
- **Ollama**
- **LLaMA 3.2**
- Python

---

<p align="center">
  <b>Built for teams that want smarter, faster, and more reliable customer support.</b>
</p>
