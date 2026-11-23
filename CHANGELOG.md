# Changelog (版本变更日志)

All notable changes to **MetaAgentFlow** will be documented in this file.
This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [v1.2.0] - 2026-11-23 (Zero-CLI & Dual-Zone Release)

### 🚀 Highlights (核心里程碑)
- **Zero-CLI Quickstart (`QUICKSTART.md`)**: 1-page copy-paste guide for users with only 2–3 web chat tabs or desktop agent windows (Claude Code / Antigravity / Cursor), requiring zero CLI setup or Python frameworks.
- **Dual-Zone Directory Separation (双区目录分离)**: every project root keeps two physically separate zones. `AI_CONTEXT/` is the AI-only memory zone; `DELIVERABLES/` holds only final artifacts for humans (`.pdf`, `.pptx`, `.mp4`, `.docx`, final figures). Scripts, intermediate CSV/JSON and logs are not allowed in `DELIVERABLES/`.
- **Painless Conversation Deletion (无痛删对话)**: before a conversation grows too long, the agent writes the latest checkpoint into `AI_CONTEXT/AI_MEMORY.md` and indexes new artifacts in `DELIVERABLES/INDEX.md`. The old conversation can then be deleted, and a new one resumes by reading `AI_MEMORY.md` first. No dependency on chat history.

### ✨ New Features (新特性)
- **Bidirectional Declarative Sync (双向声明式直连同步)**: workspace blackboard at `.agent/blackboard/sync-state.json` and `error-ledger.md`. Saying 【存档】 on the coding side packages new bugs and cases; saying 【更新】 on the skill side compiles audit rules; saying 【更新】 on the coding side reloads them.
- **Automated Dispatch (CORE-01 自动化派工)**: the master orchestrator outputs a standardized Work Dispatch Card from the task DAG, so the human no longer relays text between agents.
- **Four Iron Rules (诚实交付四大铁律)** embedded in the dispatch template: evidence before conclusions, failures must be visible, mutation-checked tests, trace to the last hop.
- **New templates**: `templates/ai_memory_template.md` and `templates/human_deliverables_index_template.md`.

### 📝 Notes (说明)
- Items above are specified in `SKILL.md` (sections 2.6, 2.7 and the dispatch template). `README.md` and `README_EN.md` describe the dual-zone layout.

---

## [v1.1.0] - 2026-11-05 (Official Open Source Release / 正式开源首发)

### 🚀 Highlights & Milestones (核心里程碑)
- **Chat-Native Multi-Agent Orchestration Protocol**: Formalized the chat-native paradigm for non-programmers, eliminating heavy Python dependencies and costly API wrappers.
- **Prompt-of-Prompts Engine**: Master Orchestrator generates strictly bounded dispatch cards, sub-prompts, and dependency manifests dynamically from a single sentence request.
- **Physical Context Anti-Bloating**: Separates complex multi-agent execution into isolated browser tabs / CLI windows, preventing context dilution and hallucination degradation beyond 20+ turns.
- **Dual-Zone Queue & ACK Compaction**: Introduces `DAILY_HANDOVER.md` with two physical regions (`Active Zone` append-only queue and `Compacted Zone` acknowledged 1-line stubs), reducing redundant tokens by 80%+.

### ✨ New Features (新特性)
- **3-Mode Adaptive Onboarding Guide**:
  - `[A] Novice Guide Mode (萌新保姆模式)`: Interactive step-by-step single-choice Q&A for first-time multi-agent users.
  - `[B] Power Dispatch Mode (熟手高效模式)`: High-density WBS task decomposition and rapid dispatch card generation.
  - `[C] Geek Workshop Mode (极客工坊模式)`: System architect mode for domain workflow customization and anchor refinement.
- **4 Standard Communication Protocol Cards**:
  1. *Check-in Protocol (开工应答卡)*
  2. *Red Flag Protocol (🚩 阻断报警卡)*
  3. *Deep Panorama Handover Protocol (深度全景存档卡)*
  4. *Succession Protocol (代际换号卡)*
- **Sleep-Cycle Natural Day Boundary**: Redefines the agent working day based on human sleep cycles rather than arbitrary midnight timestamps.
- **Autonomous Agent Self-Numbering**: Standardized `[MMDD]-[ROLE]-[ID]` tracking system for end-to-end tracing across blackboards and PRs.
- **Full Desensitized Open Source Templates**:
  - `templates/profile_template.md` (Personal facts ledger & anchor)
  - `templates/handover_template.md` (Dual-zone blackboard template)
  - `templates/workflow_spec_template.md` (Custom multi-agent pipeline specification)
  - `templates/red_flag_template.md` (Circuit breaker & fail-fast mechanism)

### 📚 Documentation (文档与教程)
- Added comprehensive bilingual `README.md` and `README_EN.md`.
- Added `docs/ARCHITECTURE.md`: Deep theoretical dive into Blackboard Architecture, Cognitive Load Theory, and Context Dilution.
- Added `docs/PROMPT_ENGINEERING_GUIDE.md`: CRIS design pattern for prompt-of-prompts synthesis.
- Added `docs/MULTI_TAB_PRACTICE.md`: Practical window/tab orchestration shortcuts and sandbox hygiene.
- Added `examples/`: End-to-end production examples for AIGC multimodal video generation, academic empirical research, and product sprint delivery.

---

## [v1.0.0] - 2026-11-04 (Internal Alpha Prototype / 概念验证原型)
- Validated core hypothesis of multi-tab physical context isolation.
- Initial implementation of the universal cold-start protocol and blackboard append-only pattern.
