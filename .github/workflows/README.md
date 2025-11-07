# QA Workflow Quick Reference

This workflow manages Quality Assurance (QA) processes for pull requests.

## Quick Start

### 🏷️ Labels

- **`qa`** - Enables QA process (adds reviewer, triggers mobile deploy)
- **`noqa`** - Skips QA process entirely
- **No labels** - Workflow will fail

### 🔄 What Happens Automatically

When you add the `qa` label:

1. ✅ `JuJoDevs` is added as a reviewer
2. 💬 `/deploy-mobile` comment is posted
3. ⏳ Workflow waits for QA approval

When you add the `noqa` label:

1. ✅ QA process is bypassed
2. ✅ Workflow passes immediately

### 📋 Requirements

For PRs with `qa` label:

- `JuJoDevs` must approve the PR
- Most recent review from `JuJoDevs` must be "Approved"

## Triggers

- Pull request: opened, reopened, labeled, unlabeled, synchronize
- Pull request reviews: submitted, dismissed

## See Also

- [Full Documentation](../docs/QA_WORKFLOW.md) - Complete workflow documentation
- [Mobile Deployment Workflow](./deploy-mobile.yml) - Related deployment workflow