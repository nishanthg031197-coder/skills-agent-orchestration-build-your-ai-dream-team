# Agent team for Mona's Project Pulse dashboard

I am using a small custom specialist team with GitHub Copilot CLI in a Codespace to orchestrate the work for Mona's Project Pulse dashboard.

- Orchestrator — Model: Claude Opus 4.7 (copilot)
  Responsibility: coordinates the project by breaking work into tasks, delegating to specialists, sequencing parallel work when safe, and verifying the final result hangs together.
  Definition: `.github/agents/orchestrator.agent.md`

- Planner — Model: Claude Opus 4.7 (copilot)
  Responsibility: researches the repository, relevant docs, dependencies, and edge cases, then produces an ordered implementation plan with file ownership, dependencies, and validation expectations.
  Definition: `.github/agents/planner.agent.md`

- Designer — Model: Gemini 3.1 Pro (copilot)
  Responsibility: designs the dashboard experience, including UX, accessibility, information hierarchy, visual styling, and responsive behavior for the Project Pulse UI.
  Definition: `.github/agents/designer.agent.md`

- Coder — Model: GPT-5.5 (copilot)
  Responsibility: implements the actual code, fixes bugs, and creates any required runnable app support files within the scope delegated by the Orchestrator.
  Definition: `.github/agents/coder.agent.md`

This team gives the project a clear split of responsibilities: planning, design, orchestration, and implementation, all managed through GitHub Copilot CLI from the Codespace environment.
