# Target Output Format Schema

Ensure the final agent output strictly matches this structure:

## Context

Current system state or motivattion for change/new feature.
Change or new feature purposes.

## Requirements
Bullet list main functions this feature provides.

## Business Rules
A table describe: Rule, Handling/Fallback

## Scenarios
Numbered list main feature's scenarios, at least 1 scenario per feature, cover happy cases.

Structure:
1. [Scenario Title]
Given [precondition/context]
When [action/event]
Then [expected outcome]
And [additional outcome]
But [exception/variation]

## Constraints

Numbered list busines rules that the data handled by this feature need to follow.

## Non-goal

Numbered list out of scope behavior, or data that will not needed by this new feature or change.

## Acceptance Criteria

Structure:

Acceptance Criteria:
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3
