# Agent Skills

A collection of custom skills for Claude — reusable frameworks that help Claude handle complex, multi-step work more effectively.

## Skills

### agent-brief

A task delegation and project scoping framework for Claude. When you hand Claude a non-trivial project, this skill teaches it to behave like a well-managed employee: clarify goals before starting, break work into checkpoints, save progress persistently, and stop at natural decision points for your approval.

**Inspired by** Ethan Mollick's [Management as AI Superpower](https://www.oneusefulthing.org/p/management-as-ai-superpower), which argues that the bottleneck with AI agents isn't the AI's capability — it's our ability to delegate well. Mollick's delegation framework depends on three variables: how long the task would take you, the probability of AI success on each attempt, and the overhead of requesting and evaluating output. The skills that matter most turn out to be the "soft" ones: scoping problems, defining deliverables, and recognizing when output is off.

This skill operationalizes that insight. It gives Claude a structured protocol for:

- **Scoping** — clarifying purpose, authority boundaries, and definition of done before starting
- **Checkpointing** — breaking work into 2–5 resumable phases with persistent outputs
- **Briefing** — creating multi-file project briefs so work survives session boundaries
- **Stopping** — pausing at decision points for human review instead of barreling ahead

#### Usage

Drop the `agent-brief` folder into your Claude skills directory. The skill triggers on phrases like "scope this out", "let's plan this", "brief me", or any request involving project kickoff and multi-phase work.

#### Structure

```
agent-brief/
├── SKILL.md              # Core skill instructions
├── assets/               # Supporting files
├── references/
│   ├── api_reference.md  # Tool API reference
│   └── templates.md      # Copy-paste brief templates
└── scripts/              # Helper scripts
```

## License

MIT