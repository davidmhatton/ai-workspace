# AI Workspace

A personal workspace for customising the AI coding agents I use day to day: rules, plugins, and whatever else each tool needs to work the way I want.

## What's here

Each top-level directory maps to a specific AI agent. Inside it sit the configuration files, rules, and extensions that shape how that agent behaves.

## Structure

```
claude/
  rules/              Writing and style rules for Claude Code
  plugins/
    david-style/      Plugin that auto-loads the style guide on every session

gemini/
  rules/              Condensed style rules for Gemini
```

Further agents and directories will appear as the workspace grows.

## Rules

The writing rules draw on Sir Ernest Gowers' *The Complete Plain Words* and a companion style guide covering formatting, structure, and length conventions. Both Claude and Gemini carry a version of these, adapted to each tool's configuration format.

## Getting started

Clone the repository and work directly. There are no build steps or dependencies to install.

```sh
git clone <repo-url>
cd ai-workspace
```

To apply the Claude rules in another project, reference them from that project's `CLAUDE.md` using `@claude/rules/style.md` and `@claude/rules/plain-words.md`.

## Installing a Claude Code plugin

Plugins in `claude/plugins/` can be installed into Claude Code's cowork mode. Each plugin directory contains a `.claude-plugin/plugin.json` manifest, hooks, and any supporting files.

To install a plugin from a local checkout of this repo:

```sh
/plugin install ./path/to/ai-workspace/claude/plugins/david-style
```

You will be prompted to choose a scope:

- **User** installs for all your projects.
- **Project** installs for all collaborators (writes to `.claude/settings.json`).
- **Local** installs for you alone in the current repo.

After installation, run `/reload-plugins` to activate it.
