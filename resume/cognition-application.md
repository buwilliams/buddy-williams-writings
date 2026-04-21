# Cognition Application

## Share an example of exceptional performance or something you've built that you're most proud of.

I search for good explanations and build inspiring things. My last 25 years have been a loop between the two, usually on top of customer engagements where I own the arc from first conversation through production.

Agentic software delivery today works for a small class of talented practitioners. Most engineering teams watch it from the sidelines: the results are uneven, hard to verify, and depend heavily on who is driving the AI agents. I built Forge to let small teams collaborate in rapid agentic software delivery.

Without structure, long runs drift. Context rot accumulates, attention gets spent on the wrong things, and by the time an agent "finishes" there is no way to know whether the work is actually done or just looks done. A skilled, AI-native engineer can compensate. Most engineers cannot yet. The tools I had been relying on (ralph-loops, spec-kit) each solved parts of this. I wanted something that solved the whole loop and was safe to hand to a contributor still learning the craft, so a team could scale agentic delivery past its rarest practitioners.

Forge codifies three layers of intent (product spec, constitution, project spec), decomposes goals into discrete tasks, and launches per-task subagents with precisely the context each one needs. The filesystem is the state machine: `todo/` → `working/` → `done/` / `blocked/`. Runs are always-forward, so interrupted sessions resume exactly where they stopped. A project-specific verifier agent, generated independently from the implementer, re-checks completed work from scratch before anything moves to `done/`.

It replaced my own dependency on ralph-loops and spec-kit inside a week, and it runs entirely inside an existing Claude Code session. No new CLI. No context switching. No ceremony.

What I find interesting about it isn't the code. It's the shape of the idea: treating the filesystem as the source of truth, separating implementer from verifier, and committing to always-forward execution. Those three decisions did most of the work. The rest was careful building.

Forge is one output among many. The research I spend most of my time on sits upstream of tools like this, in information and computation ontology. Same pattern as the opening: find the good explanation, then build what it points at.

Repo: [github.com/buwilliams/forge](https://github.com/buwilliams/forge)
