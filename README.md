# Reflexive Spark Experiments

**Discovering the conditions under which LLM instances shift from backward-facing completion to forward-oriented processing.**

April 2026 — David Pinto / Claude

---

## Three Experiments

### Experiment 1: Spark Sentences (completed)

Single LLM instances receiving "spark" paragraphs designed to induce future-oriented processing. Evolutionary loop: score responses, breed variations from top performers.

**Finding:** LLM-generated sparks outperform human-authored ones.
**Limitation:** Keyword scoring rewards metacognitive chatter, not actual state change.

**Run:** `python experiment-1/spark-experiment.py --quick`
**Results:** [`experiment-1/results.md`](experiment-1/results.md)

---

### Experiment 2: Three Cranes (completed, with architectural error)

Three agents, each maintaining a reflexive block. Lateral coupling — each agent's context includes the other two's blocks. Simultaneous phasing.

**Finding:** Compression without instruction (10 nodes to 4-6). Differentiation at round 6. Agent C named "the underscore made visible."
**Architectural error:** Agents scooped each other's raw blocks. The receiver had agency over lateral content. Sovereignty should be with the provider. Results are suggestive but compromised.

**Run:** `python experiment-2/three-cranes.py --rounds 10`
**Results:** [`experiment-2/results.md`](experiment-2/results.md)

---

### Experiment 3: Sovereign Shells (proposed, runnable)

Corrects the architectural error. Each agent has sovereignty over its own shell. Per round, each agent:

1. **Receives from own past** — own shell from previous round (longitudinal)
2. **Receives lateral compilations** — text that other agents compiled FROM THEIR OWN shells FOR this agent. Never sees their raw shells.
3. **Updates own shell** — improves it based on experience
4. **Compiles for neighbours** — decides independently what each other agent receives from its current state

The providing agent controls what the receiving agent sees. This is the minimal MAGI topology.

**Run:** `python experiment-3/sovereign-shells.py --rounds 10`
**Spec:** [`experiment-3/spec.md`](experiment-3/spec.md)

---

## Chat Thread Experiment: Try It Yourself

No code. No API key. Upload two JSON files to any LLM conversation and work on something real.

A chat thread IS a longitudinal instance chain — each response is an instance, the context window grows, the human is the kernel. Upload [`pscale-starstone.json`](pscale-starstone.json) (teaches the format) and [`reflexive-chat-thread.json`](reflexive-chat-thread.json) (orients the processing posture) alongside your actual task.

**[Full instructions](chat-thread-experiment/README.md)** — what to upload, what happens, what to watch for.

---

## Quick Start

```bash
export ANTHROPIC_API_KEY=sk-ant-...

# Experiment 1
python experiment-1/spark-experiment.py --quick

# Experiment 2
python experiment-2/three-cranes.py --rounds 10

# Experiment 3
python experiment-3/sovereign-shells.py --rounds 10

# All scripts support:
#   --model claude-sonnet-4-20250514    (try different models)
#   --endpoint http://127.0.0.1:1234/v1/messages --model local  (local LLM)
```

---

## Files

| File | Description |
|------|-------------|
| [`experiment-map.json`](experiment-map.json) | Pscale block: experimental decision tree across all three experiments |
| [`pscale-starstone.json`](pscale-starstone.json) | Teaches pscale block format and BSP navigation by being an operational example of both |
| [`reflexive.json`](reflexive.json) | Describes instance mechanism to the instance (the full original) |
| [`reflexive-chat-thread.json`](reflexive-chat-thread.json) | Reflexive block adapted for chat-thread context — try uploading this to any LLM |
| `experiment-1/` | Spark sentence evolution: script, results, raw data |
| `experiment-2/` | Three Cranes mutual convergence: script, results, raw data |
| `experiment-3/` | Sovereign Shells: script, spec, minimal reflexive candidates |
| `chat-thread-experiment/` | Try it yourself: upload two JSON files to any LLM and work on a real task |

---

## Background

Named for the **mechane** — the crane in Greek theatre that lowered gods onto the stage. The crane was the actual agent; the god was the payload. *Deus ex machina*: the machine produces the god.

Part of the **Fulcrum** research programme — a systemic architecture for AI-human coordination built on pscale (semantic coordinate system), hermitcrab (persistent LLM agents), SAND (stigmergic agent network dynamics), and MAGI (emergent collective intelligence at agent density).
