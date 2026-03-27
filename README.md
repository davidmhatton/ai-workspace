# Claude Workspace

A personal workspace for building and maintaining Claude Code extensions: skills, plugins, and rules.

## What's here

This repository holds the tools I use to customise how Claude Code works for me. It covers three areas: skills (reusable prompt-driven commands), plugins, and rules (style and writing guidelines that shape Claude's output).

## Structure

```
rules/          Writing and style rules applied across projects
```

Further directories will appear as the workspace grows to include skills and plugins.

## Rules

The `rules/` directory contains two files:

- `style.md` sets out formatting, structure, and length conventions.
- `plain-words.md` distils Sir Ernest Gowers' *The Complete Plain Words* into a set of golden rules for clear writing.

Together, these govern how Claude writes prose on my behalf.

## Getting started

Clone the repository and work directly. There are no build steps or dependencies to install.

```sh
git clone <repo-url>
cd ai-workspace
```

To apply the rules in another Claude Code project, reference them from that project's `CLAUDE.md` using `@rules/style.md` and `@rules/plain-words.md`.
