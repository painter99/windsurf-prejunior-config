# 🌊 Windsurf Pre-Junior Config

[![Windsurf IDE](https://img.shields.io/badge/Windsurf-IDE-blue?logo=codeium)](#)
[![Model Context Protocol](https://img.shields.io/badge/MCP-Enabled-green)](#)
[![KISS Principle](https://img.shields.io/badge/KISS-Compliant-orange)](#)

> **"Turn your AI from a blind code-generator into a strict Socratic mentor."**

A curated set of rules, workflows, and configurations for the [Windsurf IDE](https://windsurf.com/), specifically designed for junior developers and self-taught engineers. This setup enforces architectural thinking, strict code hygiene, and continuous learning through the "Second Brain" protocol.

## 🎯 Why does this exist?
Modern AI tools (like Cascade or Cursor) often write code *for* you, bypassing the learning process. This configuration restricts the AI, forcing it to explain the "Why", map out dependencies (using GitNexus), and wait for your approval before writing a single line of code.

## 📂 Repository Structure

```text
windsurf-prejunior-config/
├── rules/
│   └── global_rules.md       # The "Constitution" for Cascade (Copy to IDE settings)
├── workflows/
│   └── review.md             # Custom Socratic Code Review workflow
├── templates/
│   ├── mcp_config.json       # Secure MCP setup (GitNexus + GitHub + Sequential Thinking)
│   ├── .gitnexusignore       # Keep your AI's semantic graph clean
│   └── plan.md               # The local project tracker (Memento strategy)
└── README.md
```

## 🚀 How to use this setup

### 1. Global Rules (The Core)
Copy the contents of `rules/global_rules.md` into your Windsurf Global Rules settings (`Settings > Cascade Rules > Global`). Adjust the bracketed information `[like this]` to fit your persona.

### 2. Socratic Code Review
Place `workflows/review.md` into your project's `.windsurf/workflows/` directory. 
Trigger it in the Cascade chat by typing `/review`. Instead of just fixing bugs, the AI will explain the root cause and ask *you* how you want to fix it.

### 3. MCP Servers Configuration
The `templates/mcp_config.json` demonstrates how to securely connect:
1. **GitNexus:** For AST-based semantic code graphs (Blast radius analysis).
2. **GitHub MCP:** For remote repository management using securely stored environmental variables (`${env:GITHUB_PAT}`).
3. **Sequential Thinking:** For forcing the AI to break down complex logical puzzles.

### 4. The "Second Brain" Protocol
This config utilizes a highly advanced Exocortex setup. It forces the AI to read a centralized `brain.md` file from a private GitHub repository at the start of every session, allowing the AI to remember your skill level, previous mistakes, and architectural preferences across completely different local projects.

## 💡 Core Philosophies Enforced
*   **80/20 Rule:** 80% planning in Chat mode, 20% execution in Write mode.
*   **GAR Method:** Define **G**oals, **A**ttempts, and **R**oadblocks before asking for help.
*   **Docs-as-Code:** Keeping `plan.md` in the root of every project.
