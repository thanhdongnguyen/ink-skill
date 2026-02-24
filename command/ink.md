---
description: Load Ink skill and get contextual guidance for building CLI applications with React
---

Load the Ink CLI framework skill and help with any terminal user interface development task using React.

## Workflow

### Step 1: Load ink skill

```
skill({ name: 'ink' })
```

### Step 2: Identify task type from user request

Analyze $ARGUMENTS to determine:
- **Task type** (new project setup, component implementation, layout, input handling, debugging, testing)
- **Complexity** (simple component, complex layout, full app)

Use decision trees in SKILL.md to select correct reference files.

### Step 3: Read relevant reference files

Based on task type, read from `references/<area>/`:

| Task | Files to Read |
|------|---------------|
| New project setup | `core/REFERENCE.md` + `core/configuration.md` |
| Display text/content | `components/text.md` + `components/utilities.md` |
| Layout/containers | `components/box.md` + `layout/REFERENCE.md` |
| Handle keyboard input | `hooks/input.md` |
| App lifecycle/exit | `hooks/app-lifecycle.md` + `core/api.md` |
| Focus management | `hooks/focus.md` |
| Stdin/Stdout/Stderr | `hooks/stdio.md` |
| Write tests | `testing/REFERENCE.md` |
| Screen reader support | `accessibility/REFERENCE.md` |
| Debug/troubleshoot | `core/gotchas.md` |
| Common patterns | `core/patterns.md` + `layout/patterns.md` |

### Step 4: Execute task

Apply Ink-specific patterns and APIs from references to complete the user's request.

### Step 5: Summarize

```
=== Ink Task Complete ===

Files referenced: <reference files consulted>

<brief summary of what was done>
```

<user-request>
$ARGUMENTS
</user-request>
