---
name: beautiful-html-templates
description: >
  A library of 34 highly aesthetic HTML slide templates designed so that any coding agent
  can pick the right one and produce a beautiful deck on the user's behalf, automatically.
  Includes full-deck templates, index.json matching, and live preview protocols.
---

# Beautiful HTML Templates Library

A library of reusable HTML slide templates designed so that any coding agent can pick the right one and produce a beautiful deck on the user's behalf, automatically.

Agents using the library should read [`AGENTS.md`](./AGENTS.md). It's the operating manual: how to read `index.json`, match the user's brief to a template, clone it, and adapt the content.

## Workflow Overview
1. Match user occasion & mood against `index.json`.
2. Pick 3 distinct candidates.
3. Generate title-slide previews with user's real topic.
4. Clone chosen template into workspace.
5. Populate real content while preserving visual system and design tokens.
