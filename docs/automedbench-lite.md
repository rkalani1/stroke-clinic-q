# AutoMedBench-Lite Gate for Stroke Clinic Q Updates

Use this gate before accepting AI-generated changes to question text, answer logic, clinical references, disclaimers, or public-demo UI copy.

This gate evaluates workflow discipline only. It does not make the page a clinical decision tool, official educational system, or source of truth.

## S1 Plan

- Identify the exact question, answer, source note, or UI element being changed.
- State whether the change affects educational content, answer logic, presentation, or compliance text.
- Define stop conditions for missing source support, conflicting guidance, or privacy risk.

## S2 Setup

- Inspect `index.html` and `COMPLIANCE.md`.
- Identify public source material or existing repo context supporting the change.
- Confirm examples are synthetic, public, or de-identified.

## S3 Validate

- Map every clinical statement to a source or existing approved context.
- Confirm answer choices and feedback do not overclaim bedside or institutional use.
- Check the page manually after edits.
- Confirm no PHI, real clinical details, learner records, credentials, or confidential institutional content are introduced.

## S4 Execute

Make only the scoped change after S1-S3 are complete. Preserve demo-only and no-PHI boundaries.

## S5 Submit

Report changed files, source trace, manual checks, residual clinical review need, and no-PHI confirmation.

## One-Shot Prompt

```text
Apply the stroke-clinic-q AutoMedBench-Lite gate. Write S1 Plan, S2 Setup, and S3 Validate before editing. Then execute the scoped change and submit changed files, source trace, manual page checks, residual clinical review need, and no-PHI confirmation. Stop if source support or privacy validation cannot be completed.
```
