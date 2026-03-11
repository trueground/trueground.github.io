# Trueground

**AI-native research pipeline. Published weekly at [trueground.github.io](https://trueground.github.io).**

Findings that challenge what the field currently believes. Practitioner discoveries that never made the changelog. The world through the lens of what AI is actually changing.

---

## What it does

Four agents run in parallel each week:

| Agent | Focus |
|---|---|
| Reasoning & inference | CoT faithfulness, test-time compute, mechanistic interpretability |
| Architecture & training | Novel architectures, training paradigms, data efficiency, self-improvement |
| Agents, multimodal & science | AI agents, memory, video, drug discovery, formal math |
| Practitioner discoveries | Things people found while *using* Claude/AI — Reddit, HN, Discord, Twitter |

A synthesis agent groups findings into cross-cutting themes, ranks by significance (not coverage), and identifies the single most important finding of the week.

Output is a self-contained HTML file deployed to GitHub Pages.

## Editorial principle

Coverage is not significance. The most important findings are systematically underrepresented in mainstream AI discourse because they are negative results, cross-domain, or threatening to current product narratives.

This pipeline inverts that: negative results rank higher, mechanistic findings rank higher, findings that would require practitioners to change behavior rank highest.

## Running

```bash
pip install -r requirements.txt
export ANTHROPIC_API_KEY=...

python run.py                        # full run + deploy
python run.py --no-deploy            # local preview only
python run.py --model claude-opus-4-6  # higher quality
```

## Structure

```
agents/                  Agent prompt files
  reasoning_inference.md
  architecture_training.md
  agents_science.md
  practitioner_discoveries.md
  synthesizer.md
lenses/
  ai-research-signal.md  Domain lens: the editorial philosophy as a decision procedure
docs/                    Generated HTML (served by GitHub Pages)
run.py                   Orchestrator
```

## Branches

- `main` — source code
- `gh-pages` — deployed output, auto-updated by `run.py`
