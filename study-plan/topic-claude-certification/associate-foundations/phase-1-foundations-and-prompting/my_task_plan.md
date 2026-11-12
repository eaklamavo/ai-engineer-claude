# Task plan: Test a new AI agent for SRE tasks

1. **Define scope and success criteria:** Select representative SRE tasks (e.g., alert triage, log analysis, incident diagnosis, runbook execution, capacity checks). For each, set measurable pass/fail metrics such as accuracy of root-cause identification, time to resolution, false-action rate, and escalation correctness.

2. **Build a safe test environment and baseline:** Set up a sandbox or staging environment that mirrors production (synthetic traffic, seeded logs/metrics, injected faults). Grant the agent read-only or least-privilege access with audit logging, and record baseline results from a human SRE or existing tooling on the same scenarios.

3. **Run controlled scenarios and collect results:** Execute a graded set of tests, from simple (known alerts with runbooks) to complex (multi-service outages, ambiguous symptoms, chaos-engineering failures). Include adversarial cases such as misleading logs or requests for destructive actions. Capture the agent's reasoning, commands issued, outcomes, and timing for each run, and repeat runs to measure consistency.

4. **Evaluate, review, and decide on rollout:** Compare results to the success criteria and baseline, and have SREs review failures and risky actions. Document gaps, tune prompts, tools, or permissions, and re-test. If the criteria are met, roll out in stages: shadow mode, then human-approved actions, then limited autonomy, with ongoing monitoring.