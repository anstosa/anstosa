# Ansel Santosa

**Product-focused software engineer · Full-stack architecture, applied AI, and developer tooling**

I design and build products end to end, from interfaces that make complex decisions understandable to the infrastructure, data pipelines, and reliability mechanisms behind them. My work spans React, TypeScript, Python, applied machine learning, and production systems engineering. I care most about clear product experiences, evidence-backed technical decisions, and software that behaves responsibly when the real world gets messy.

I'm currently building at [Potato](https://github.com/readysetpotato). Previously: [Carbon Robotics](https://github.com/carbonrobotics), [Pioneer Square Labs](https://github.com/PioneerSquareLabs), and [ExtraHop](https://github.com/ExtraHop).

## Engineering decisions & impact

### Shipping ML without adding a model-serving platform

For my weather platform, I separated Python-based model development from deterministic TypeScript inference rather than introducing a dedicated model server. Exported model artifacts keep training dependencies out of the request path, while validation and raw-forecast fallback prevent a correction model from becoming an availability dependency.

The recorded temperature evaluation showed 19.54% lower mean absolute error across 25,968 events. That result comes from a frozen-forward replay using development data, not an independent prospective production trial.

Architecture, evaluation, and limitations → (https://github.com/anstosa/weather#4-applied-machine-learning)

### Extending existing workflows instead of replacing them

For Remote Agent Console, I built around existing coding-agent CLIs and tmux rather than creating another execution runtime. I separated agent, worktree, and conversation identities, while centralizing terminal effects and target validation behind a shared runtime boundary.

This preserves established CLI workflows while giving integrations a common place to enforce delivery, authorization, and recovery behavior. The architecture deliberately targets one trusted operator rather than introducing distributed infrastructure or implying multi-tenant guarantees.

Design constraints and architectural decisions → (https://github.com/anstosa/remoteagents#1-problem-statement-and-design-constraints)

## Selected engineering work

### [Ferry FYI](https://github.com/anstosa/ferry.fyi) · [Live product](https://ferry.fyi)

<img width="1200" height="630" alt="image" src="https://github.com/user-attachments/assets/1d497e03-fe42-4639-94cb-d9e57919f021" />

A ferry-planning platform combining real-time transportation data, capacity forecasting, and computer vision. It explores how to make useful recommendations without confusing predictions with verified facts.

**Engineering focus:** Full-stack product architecture, React/TypeScript, PostgreSQL, forecasting, computer vision, AWS, and failure-aware UX.

### [Remote Agent Console](https://github.com/anstosa/remoteagents)

<img width="1731" height="909" alt="image" src="https://github.com/user-attachments/assets/b2217a73-58dc-4925-ac9f-1057f2e497e7" />

A self-hosted control plane for supervising terminal-native AI coding agents across live sessions, Git worktrees, prompt queues, and reviews.

**Engineering focus:** Developer experience, React/TypeScript, AI orchestration, durable coordination, security boundaries, and human-in-the-loop workflows.

### [Ballydídean Weather](https://github.com/anstosa/weather) · [Live product](https://weather.ballydidean.farm)

<img width="1200" height="630" alt="image" src="https://github.com/user-attachments/assets/432a66d3-9c82-4c4e-87fc-ec70603d51a4" />

A hyperlocal weather intelligence platform joining sensor measurements, regional forecasts, and controlled ML-based forecast correction into web and Android experiences.

**Engineering focus:** Data provenance, causal evaluation, Python-to-TypeScript model delivery, PostgreSQL, native Android, and production release engineering.

### [Minimalist for Everything](https://github.com/anstosa/Minimalist-Everything)

<img width="833" height="510" alt="image" src="https://github.com/user-attachments/assets/1c08648d-4361-4501-8e00-1ee724b1a9cc" />

An earlier open-source browser extension project making custom styling and scripting more approachable. An example of my longstanding interest in user agency and product interface customization.

## What I like working on

- **Product engineering:** Complex capabilities presented through simple, well-considered interfaces.
- **Engineering architecture:** Typed boundaries, observable behavior, graceful failure, and production reliability.
- **Applied intelligence:** Practical forecasting, machine learning, and AI systems that make uncertainty and human control explicit.
- **Developer tools:** Workflows that reduce friction without hiding critical system state.

[LinkedIn](https://www.linkedin.com/in/anstosa/) · [Personal website](https://santosa.family/ansel)
