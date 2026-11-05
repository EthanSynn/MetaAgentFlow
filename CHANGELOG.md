# Changelog (版本变更日志)

All notable changes to **MetaAgentFlow** will be documented in this file.
This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
