# Enterprise AI Tool Adaptation and Capability Retention

PE6203 Group Project 4 investigates how an AI agent adapts when its external tools change. We compare no update, full rewrite, and selective patch of tool knowledge using MCPEvol-Bench. Base model weights remain unchanged.

**Repository status:** the repository is being assembled. Evidence archives and their provenance are prepared here; the six assigned source modules are pending member import. A runnable source checkout requires those imports and dependency installation.

## Evidence and results

The [evidence index](docs/EVIDENCE.md) links all three original experiment archives, checksums, and source releases. The [machine-readable index](artifacts/evidence/releases.json) preserves their provenance. The archives are mirrors of completed experiments, not new runs.

Three rounds contain 486 scored observations with all failures retained. Only R1 + R3 support a 324-observation descriptive comparison over 18 distinct tasks; R2 stays separate because resource lists differ. Selective patch uses 65.1% fewer update tokens than full rewrite in that comparison, while total recorded update/agent/judge tokens are 5.6% higher. These are descriptive results, not universal superiority or significance claims.

## Shared project structure

| Path | Content after member imports |
|---|---|
| `tool_adapt/` | Agent execution, MCP connections, knowledge adaptation, metrics |
| `configs/` | Frozen experiment settings and model capacity configuration |
| `scripts/` | Setup, execution, scoring, evidence checks, and reporting |
| `tests/` | Update-boundary, protocol, failure, and packaging checks |
| `artifacts/` | Tool inventories, metrics, audit receipts, and evidence index |
| `docs/` | Report source, method, cases, reproduction, and evidence guide |
| `output/pdf/` | Integrated report and historical original report |
| `archive/` | Preserved historical development files and progress snapshots |

These shared directories form one system.

## Team responsibilities

| Part | Member | Responsibility |
|---|---|---|
| A | SU YANG | Agent execution and tool calls |
| B | LIU ZHEYUAN | Tool knowledge and selective adaptation |
| C | HE YUJIE | Experiment design, execution, and reproduction |
| D | SHISHUYI | Metrics, recovery, retention, and cost |
| E | LIN GENXIN | Failure cases and score/evidence review |
| F | PAN JUNKUN | Report integration and delivery consistency |

## Provenance and reproduction scope

The original source and experiment history are preserved at [the source repository](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation). The benchmark is [MCPEvol-Bench](https://github.com/Octobrist/MCPEvol-Bench), pinned to revision `888c779a0fe735f612ca62bdd1fdd7c9e6bf8701`. Actor/updater: local Qwen3 4B; judge: local Qwen2.5 7B through llama.cpp. No paid API is required; model weights and runtime dependencies are installed separately.

Project documents are English. Frozen data, model messages, logs, contracts, and receipts retain original bytes and language. Development and evidence review used AI assistance. Saved plans and automatic scores must be checked against actual calls and artifacts.
