# Fork automation

- CI runs for pull requests and pushes to `personal/main`.
- `main` remains a clean mirror of `upstream/main` and is not a development or deployment branch.
- Release, relay, and mobile deployment workflows are disabled by default. They require the repository variable `FORK_CD_ENABLED` to be set to `true` before their jobs can run.
- The release and relay workflows are manual-dispatch only. Re-enabling scheduled or tag-driven releases should be an explicit fork decision.
- GitHub's default branch should be `personal/main` so Actions uses the fork-safe workflow definitions rather than the pristine upstream mirror.
