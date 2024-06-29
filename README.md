# Agentic Theory of Mind Evals

This repo runs evals with the objective of studying the impact of AI agency on Theory of Mind capabilities.
See [the project description document](https://docs.google.com/document/d/1WiNid0w3vMDV-IVQrIUEoCR1aHjYDqBb3rib2VYqnbk/edit?usp=sharing) for more details.

The evals tooling used is the [UK AI Safety Institute Inspect framework](https://ukgovernmentbeis.github.io/inspect_ai/).

### Install

Install required python packages using
```bash
pip install -r requirements.txt
```

### Configuration

First, copy the .env template
```
cp .env.template .env
```

Then fill desired values. Current configuration values
| Variable  | Description  |
|---|---|
| ANTHROPIC_API_KEY  | See https://console.anthropic.com/settings/keys |

Source the values into your shell
```bash
set -a
source .env
set +a
```

### Execute

Can execute an eval using:

```bash
inspect eval theory_of_mind.py --model {desired-model}
```

For example, to run using the Anthropic Haiku model
```bash
inspect eval theory_of_mind.py --model anthropic/claude-3-haiku-20240307
```

### Examine Results
To view the results of the evals, run
```bash
inspect view
```