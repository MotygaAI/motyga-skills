# Motyga Skills

Open, curated **skills** (reusable agent recipes) for [Motyga](https://motyga.com) agents and the
[Motyga Code](https://github.com/motyga/motyga-code) VS Code extension.

A *skill* is a small, model-agnostic playbook: a system/instruction recipe plus optional examples and
tool permissions that turn an agent into a focused specialist (code review, deep research, data
analysis, …). Skills run on **any** model available through Motyga (or your own BYOK/local model).

> The skills idea is inspired by **[NVIDIA Skills](https://build.nvidia.com/skills)** — inspiration
> only, no content is copied. Vendor-specific or proprietary prompts are never accepted here.

## Layout

```
skills/
  <skill-id>/
    skill.yaml     # manifest (see schema below)
    SKILL.md       # the instruction recipe (the actual skill)
    examples/      # optional input/output examples
```

## Manifest (`skill.yaml`)

```yaml
id: code-review
name: Code Review
version: 0.1.0
summary: Walk a diff/PR, find bugs, risks and style issues; return notes with fixes.
category: coding            # coding | research | content | data | creative | security
authors:
  - name: Motyga
    url: https://motyga.com
license: Apache-2.0
attribution:
  inspired_by:
    - { name: NVIDIA Skills, url: https://build.nvidia.com/skills, note: "inspiration only" }
compatibility:
  agents: [motyga-code, openai-compatible]
  models: [any]
files:
  entrypoint: SKILL.md
  examples: examples/
permissions:
  filesystem: read          # none | read | read-write
  shell: optional           # none | optional | required
  network: optional
tags: [coding, review]
```

## Use

- **Motyga Code:** point the extension at a skill folder, or paste `SKILL.md` as the system recipe.
- **API (`/v1`):** prepend `SKILL.md` as the system message when calling any model via Motyga.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). One skill per directory, `skill.yaml` + `SKILL.md`, your own
content only, no secrets, Apache-2.0.

## License

[Apache-2.0](LICENSE).
