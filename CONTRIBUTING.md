# Contributing to Soroban CrashLab

Thanks for contributing. This project is maintainer-first and contributor-friendly: we optimize for clear issue scope, reproducible changes, and fast review cycles.

## Development setup

### Frontend

```bash
cd apps/web
npm install
npm run dev
```

### Core crate

```bash
cd contracts/crashlab-core
cargo test
```

## Branch and PR flow

1. Create a branch from `main` named `feat/<short-name>` or `fix/<short-name>`.
2. Keep PRs focused on one issue.
3. Link the issue in the PR description using `Closes #<number>`.
4. Include test evidence and reproduction notes for behavior changes.

## Quality bar

- changes are readable and maintainable
- no dead code or placeholder logic in merged PRs
- tests cover the introduced behavior
- docs are updated when user-facing behavior changes

## Issue Complexity Rubric

### Trivial
**Definition:**
Small, self-contained tasks that require minimal context. Often focused on straightforward updates, UI tweaks, or simple configuration mapping.

**Characteristics:**
- Size of change is small (usually 1-2 files)
- Very low risk of regression
- No complex architectural or design decision-making needed
- Straightforward testing

**Examples:**
- Implement seed schema validator
- Build run history table UI
- Add markdown rendering for issue-ready reports

---

### Medium
**Definition:**
Standard features or enhancements requiring moderate context. Involves implementing distinct workflows, new components, or integrating existing services.

**Characteristics:**
- Size of change is moderate (may touch multiple files in one area)
- Moderate risk requiring specific test coverage for new failure modes
- Requires some component-level design choices within established patterns
- Clear boundaries of impact

**Examples:**
- Build failure classification taxonomy
- Add replay command for single seed
- Add signature trend charts

---

### High
**Definition:**
Complex features, fundamental behavior changes, or cross-cutting architectural work. Requires deep context of the system and rigorous validation.

**Characteristics:**
- Size of change is significant (modifies core execution paths)
- High risk or broad impact across the codebase
- Involves novel algorithms, complex state management, or deep architectural design
- Requires extensive test coverage, performance benchmarking, or careful review

**Examples:**
- Add authorization mode matrix runner
- Export failing seed as Rust regression fixture
- Implement seed prioritization by novelty

## Review expectations

- maintainers prioritize active Wave issues during the sprint window
- contributors should respond to review comments within 24 hours when possible
- unresolved architectural debates should move to issue discussion to keep PRs focused
