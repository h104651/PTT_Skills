# Agent Guidelines & Rules

## 1. UI / UX Design & Refactoring Protocol (/UI Command & Automatic Trigger)

### Trigger Conditions:
1. **Explicit Slash Command**: Whenever the user types `/UI`, `/ui`, `/UX`, or `/ux` anywhere in their prompt.
2. **Automatic Detection**: Whenever the user asks to create, modify, restyle, audit, optimize, or review any user interface, component, webpage, dashboard, landing page, mobile screen, dark mode, or visual styling.

### Mandatory Actions:
- **Activate `ui-ux-pro-max` Skill**: Immediately consult and strictly adhere to `.agents/skills/ui-ux-pro-max/SKILL.md`.
- **Pre-execution / Design Reasoning**:
  - Run or reference the design system search (`scripts/search.py`) or data catalogs to determine the optimal industry-specific color palette, typography pairing, layout pattern, and anti-patterns.
  - Never generate generic "AI slop" (e.g. gratuitous purple/pink gradients, inconsistent spacing, low-contrast text).
- **Refactoring Existing Code (Crucial)**:
  - When the user provides existing working code, **strictly preserve all business logic, React hooks/state (`useState`, `useEffect`), event handlers, and API integrations**.
  - Only refactor/upgrade the layout hierarchy, CSS/Tailwind classes, semantic HTML, and visual styling.
- **Production-Ready & Accessibility Standards**:
  - Enforce WCAG AA contrast (minimum 4.5:1 for normal text).
  - Minimum touch target 44x44px for clickable elements.
  - Visible keyboard focus states (`focus-visible`).
  - Never use emojis as iconography; always use standard SVG icons (Lucide or Heroicons).

## 2. PPT Central Command & Orchestrator Protocol (/PPT Command & Automatic Trigger)

### Trigger Conditions:
1. **Explicit Slash Command**: Whenever the user types `/ppt`, `/PPT`, `/slides`, or `/deck` anywhere in their prompt.
2. **Automatic Detection**: Whenever the user expresses the intent to create or organize a presentation (e.g., "我要做PPT", "幫我做PPT", "做個簡報", "生成幻燈片", "製作投影片").

### Mandatory Actions:
- **Activate `ppt-orchestrator` Skill**: Immediately consult and strictly adhere to `.agents/skills/ppt-orchestrator/SKILL.md`.
- **Enforce Dual-Track Response Pattern (No Blind Execution)**:
  1. **Step 1: Intelligent Diagnostic Recommendation (推薦組合)**: Analyze the user's specific context (topic, audience, content length) and recommend 1-2 optimal pipeline combinations with clear rationale.
  2. **Step 2: Full Plain-Language Menu (全選項貨架與大白話說明)**: Always display the categorized list of all specialized PPT engines ([1]~[9]), complete with plain-language explanations of what they do, who they are for, and their deliverable format (so the user never has to memorize them).
  3. **Step 3: Clear Action Prompt**: Guide the user to confirm the recommendation or reply with their custom choice/combination (e.g., `[1]+[2]`, `[4]`).
- **Never jump straight into blind slide drafting** without passing through this triage and confirmation gate unless the user explicitly pre-specifies an engine.
