# amplify-fusion-java-service

A Claude skill for generating production-ready Java service code for [Axway Amplify Fusion](https://docs.axway.com/bundle/amplify-fusion) pipelines.

[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-blue)](https://claude.ai/code)

## What it does

When installed, this skill teaches Claude how to write Fusion-compatible Java services — handling the `dataIn`/`dataOut` map convention, type casting, null safety, and the constraints of the shared data plane. Ask Claude to build a Java service for any pipeline task and it will produce ready-to-paste code along with the input/output variable definitions and a test example.

## Usage

Once installed, just describe what you need:

> "Create a Fusion Java service that filters a document array by category name"

> "Write a Fusion Java service to convert an epoch timestamp to ISO 8601"

> "Build a Fusion Java service that validates and parses a JSON string"

Claude will output:
- **Input/Output variable definitions** to configure in the Fusion UI
- **Complete Java code** to paste into the code editor
- **A test input example** to use with the built-in Test button

## Shared vs. dedicated data plane

By default, generated code targets the **shared data plane** — no external libraries, only Axway-whitelisted classes (`java.util`, `javax.json`, `java.time`, `java.net`, etc.). If you're on a dedicated data plane and need third-party libraries, say so explicitly and Claude will include JAR download links and dependency notes.

## Installation

Download `amplify-fusion-java-service.skill` and install it via your Claude skills settings.

## Contents

```
amplify-fusion-java-service/
├── SKILL.md                      # Core skill instructions
└── references/
    ├── whitelist.md              # Full shared data plane class whitelist
    └── patterns.md               # 12 copy-paste code patterns
```
