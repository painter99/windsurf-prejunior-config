# 🌊 Windsurf Pre-Junior Config

[![Windsurf IDE](https://img.shields.io/badge/Windsurf-IDE-blue?logo=codeium)](#)
[![Model Context Protocol](https://img.shields.io/badge/MCP-Enabled-green)](#)
[![KISS Principle](https://img.shields.io/badge/KISS-Compliant-orange)](#)

> **"Turn your AI from a blind code-generator into a strict Socratic mentor."**

A curated set of rules, workflows, and configurations for the [Windsurf IDE](https://windsurf.com), specifically designed for junior developers and self-taught engineers. This setup enforces architectural thinking, strict code hygiene, and continuous learning through the local Exocortex protocol.

## 🎯 Why does this exist?
Modern AI tools (like Cascade or Cursor) often write code *for* you, bypassing the learning process. This configuration restricts the AI, forcing it to explain the "Why", map out dependencies (using GitNexus), and wait for your approval before writing a single line of code.

## 📖 The Philosophy: From Chatbot to Agent
Why should a beginner switch to an Agentic IDE? It solves the friction of context switching and prevents "Tutorial Hell."
Instead of copy-pasting code from a browser, this setup integrates the AI directly into your file system, forcing it to understand your architecture before suggesting changes.

👉 **[Read the full Workflow Manifesto & Methodology](WHY_AGENTIC.md)**

## 📂 Repository Structure

```text
windsurf-prejunior-config/
├── rules/
│   └── global_rules.md       # The "Constitution" for Cascade
├── skills/
│   └── prompt-snr-optimizer/ # Example of custom Cascade Skill
├── workflows/
│   └── review.md             # Custom Socratic Code Review workflow
├── templates/
│   ├── mcp_config.json       # Secure MCP setup
│   ├── .gitnexusignore       # Keep your AI's semantic graph clean
│   └── plan.md               # The local project tracker
├── WHY_AGENTIC.md            # Detailed Manifesto
└── README.md
```

## 🚀 How to use this setup

### 1. Global Rules (The Core)
Copy the contents of `rules/global_rules.md` into your Windsurf Global Rules settings (`Settings > Cascade Rules > Global`).

### 2. Socratic Code Review
Place `workflows/review.md` into your project's `.windsurf/workflows/` directory. 
Trigger it in the Cascade chat by typing `/review`. Instead of just fixing bugs, the AI will explain the root cause and ask *you* how you want to fix it.

### 3. Custom AI Skills
I provide curated agentic skills (e.g., `prompt-snr-optimizer`) in the `skills/` directory. You have two options for using them:
- **Global (Recommended):** Copy the skill folder to `~/.codeium/windsurf/skills/` (Linux/Mac) to use it across all your projects.
- **Local:** Copy the skill folder to `.windsurf/skills/` inside a specific project to restrict its usage.

### 4. MCP Servers Configuration
The `templates/mcp_config.json` demonstrates how to securely connect:
1. **GitNexus:** For AST-based semantic code graphs (Blast radius analysis).
2. **GitHub MCP:** For remote repository management using securely stored environmental variables (`${env:GITHUB_PAT}`).
3. **Memory Service (`mcp-memory-service`):** A high-performance SQLite (`sqlite-vec`) backend providing your local Knowledge Graph (Exocortex 2.0). It tracks your skills, preferences, and goals using semantic flat-text tags.
4. **Sequential Thinking:** For forcing the AI to break down complex logical puzzles.

### 5. The Exocortex Protocol
This config utilizes a highly advanced local memory setup. It forces the AI to read an SQLite vector database at the start of every session (via `mcp3_memory_search`), allowing the AI to seamlessly remember your skill level, previous mistakes, and architectural preferences locally. It achieves sub-5ms query times by replacing the legacy JSONL graph with semantic embedding models.

## 💡 Core Philosophies Enforced
*   **80/20 Rule:** 80% planning in Chat mode, 20% execution in Write mode.
*   **GAR Method:** Define **G**oals, **A**ttempts, and **R**oadblocks before asking for help.
*   **Docs-as-Code:** Keeping `docs/plan.md` in every project (local only).
