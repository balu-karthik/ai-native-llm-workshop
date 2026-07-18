# AI-Native LLM Workshop

A hands-on workshop covering the core prompt engineering techniques used to get reliable, high-quality output from large language models — implemented as small, runnable Python scripts you can study, run, and adapt.

Forked from [`amitpandeygit/llm-workshop`](https://github.com/amitpandeygit/llm-workshop), with additional demos and updates (including a switch of the CoVe demo from the Anthropic API to the Google Gemini API).

## What's inside

The `code/` directory contains one script per prompting technique:

| Script | Technique |
|---|---|
| `zero_shot.py` | Zero-shot prompting — asking the model to perform a task with no examples |
| `few_shot.py` | Few-shot prompting — guiding the model with a small number of examples |
| `role_prompting.py` | Role prompting — assigning the model a persona/role to shape its output |
| `chain_of_thought.py` | Chain-of-thought prompting — eliciting step-by-step reasoning |
| `self_consistency.py` | Self-consistency — sampling multiple reasoning paths and taking a consensus answer |
| `react.py` | ReAct — interleaving reasoning and tool/action steps |
| `directional_stimulus.py` | Directional stimulus prompting — steering output using hint keywords/cues |
| `cove_desk.py` | Chain-of-Verification (CoVe) — having the model verify and correct its own answers |

> Root-level files (setup guide, slide decks, etc.) aren't fully captured here — let me know the exact filenames and I'll add them to the structure below.

## Prerequisites

- Python 3.9+
- pip
- API key(s) for the LLM provider(s) used by the scripts (Anthropic and/or Google Gemini, depending on the demo)

## Setup

```bash
# Clone the repo
git clone https://github.com/balu-karthik/ai-native-llm-workshop.git
cd ai-native-llm-workshop

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### API keys

Set the relevant environment variable(s) before running the scripts:

```bash
export ANTHROPIC_API_KEY="your-key-here"
export GOOGLE_API_KEY="your-key-here"
```

## Running the demos

Each script is self-contained and can be run individually from the `code/` directory:

```bash
cd code
python3 zero_shot.py
python3 few_shot.py
python3 chain_of_thought.py
python3 self_consistency.py
python3 react.py
python3 role_prompting.py
python3 directional_stimulus.py
python3 cove_desk.py
```

## Workshop goals

By the end of this workshop, you should be able to:

- Recognize and apply the major prompt engineering techniques (zero-shot, few-shot, CoT, self-consistency, ReAct, role prompting, directional stimulus, CoVe)
- Understand the tradeoffs between techniques (cost, latency, reliability)
- Know when to reach for verification/self-consistency methods to reduce hallucination
- Compare behavior across different model providers (Anthropic, Gemini)

## Project structure

```
ai-native-llm-workshop/
├── README.md
├── requirements.txt
└── code/
    ├── zero_shot.py
    ├── few_shot.py
    ├── role_prompting.py
    ├── chain_of_thought.py
    ├── self_consistency.py
    ├── react.py
    ├── directional_stimulus.py
    └── cove_desk.py
```

## Attribution

This project is a fork of [`amitpandeygit/llm-workshop`](https://github.com/amitpandeygit/llm-workshop). See that repository for original licensing and contribution terms.

## Contributing

Suggestions and corrections are welcome via issues or pull requests.
