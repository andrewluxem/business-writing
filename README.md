# business-writing

A small, static agent skill that turns a draft or notes into decision-useful business writing and makes its editorial judgment visible.

It produces three artifacts:

- **Edited Business Document plus Change Scorecard**: preserves supported facts, moves the bottom line first, records representative edits, and flags every meaning change.
- **New Business Document plus Change Scorecard**: turns notes into a document for a named reader and outcome, with visible evidence, owner, and date gaps instead of guesses.
- **Writing Audit**: scores clarity of thought, document structure, and sentence mechanics, then prioritizes the three repairs that matter most.

It executes the [Business Writing playbook](https://www.andrewluxem.com/playbooks/business-writing). The playbook teaches the standard. This skill applies it to a working document.

**Static by construction: no dependencies, executable code, telemetry, network calls, remote instructions, auto-update, scheduled work, or background behavior.** It reads only the files in its own skill folder. Nothing happens until a user or agent invokes it.

## Install

Clone and copy the skill into Claude Code:

```bash
git clone https://github.com/andrewluxem/business-writing.git
cp -r business-writing/skills/business-writing ~/.claude/skills/
```

Or install it as a Claude Code plugin:

```text
/plugin marketplace add andrewluxem/business-writing
/plugin install business-writing@business-writing
```

For clients that install from an archive, keep using the versioned [business-writing v1.0.0 ZIP](https://www.andrewluxem.com/downloads/business-writing-v1.0.0.zip).

## Invoke it

```text
Edit this memo to the business writing standard
Write a decision memo from these notes
Audit this draft for clarity, structure, and sentence mechanics
```

Naming the skill is always valid: `use the business-writing skill to edit this memo`.

## Files

```text
.claude-plugin/
  plugin.json
  marketplace.json
skills/business-writing/
  SKILL.md
  meta.yaml
  LICENSE.md
  assets/
  references/
README.md
LICENSE
```

- `SKILL.md` defines the modes, workflow, and guardrails.
- `assets/` contains the edited-document template, change scorecard, and audit scorecard.
- `references/` contains the editing standard used for structural edits and audits.
- `meta.yaml` records version, access tier, invocation tests, and changelog.

## Versioning

Plugin installation is version-pinned. When behavior changes, update the version consistently in `SKILL.md`, `meta.yaml`, and `.claude-plugin/plugin.json`, then add a changelog entry. Reinstalling is an explicit update; this repository never auto-updates itself.

## License

MIT. See [LICENSE](LICENSE). The canonical skill folder carries the same authorization in [skills/business-writing/LICENSE.md](skills/business-writing/LICENSE.md).

---

## More playbooks

This skill packages one playbook from the free library at [github.com/andrewluxem/playbooks](https://github.com/andrewluxem/playbooks). Every playbook is free to read, with no email required.
