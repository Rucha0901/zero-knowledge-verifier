# Agent Architecture & Topology

Zero-Knowledge Verifier Agent employs a modular multi-agent architecture with strict supervisory boundaries, deterministic resource budgeting, and zero prompt-leakage contracts.

## Multi-Agent Roles

- **circuit-proof-analyzer**: Performs primary technical analysis and forms candidate plans. Role: maker.
- **soundness-completeness-critic**: Audits diagnostic findings and verifies safety invariant constraints. Role: checker.
- **compliance-auditor**: Verifies regulatory policies and logs cryptographically signed traces. Role: auditor.
- **task-executor**: Dispatches verified interventions to external environments. Role: executor.

## Segregation of Duties

The system enforces strict segregation between plan generation and verification:
- The maker role is held by circuit-proof-analyzer.
- The checker role is held by soundness-completeness-critic.
These roles are strictly partitioned and cannot be executed by the same agent.

## Capabilities
- Autonomous security diagnostics and domain-specific reasoning.
- Multi-agent verification with mathematical invariant checks.
- Cross-runtime portability across OpenAI SDK, CrewAI, Claude Code, and Lyzr.

## Constraints
- Zero raw user prompt leakage to unencrypted external logs.
- Hard resource budget caps to prevent recursive invocation loops.
- All high-impact actions must pass independent checker review before release.
