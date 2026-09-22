# websiteDOS2019 — Agent State

## Stack
- **Language**: Python
- **Dependencies**: socket, threading (standard library)
- **Type**: Legacy utility — HTTP flood / DoS stress-test script (2019)

## Last change — 2026-09-22

Fixed broken `label.yml` workflow that was blocking all Dependabot PRs. Same
root cause as the other sgNRIC*/sgNumbers*/sgPhone* repos: two bugs in
`.github/workflows/label.yml`:

1. **Wrong config path** — workflow pointed to `.github/labeler.yml` (does not
   exist); actual labels file is `.github/labels.yml`.
2. **Missing permissions block** — `permissions: pull-requests: write` was
   absent, causing the label step to fail with a 403.

Both fixed identically. Label check now passes. Dependabot PR #54 was
subsequently merged.

## Status

DONE — label workflow fixed, PR #54 merged.
Ended because: task complete.

## Notes
- ddos.py contains a DoS flood script — target IP is `0.0.0.0` (placeholder, not a live target)
- ddos.pyw is the windowless variant
- No hardcoded credentials or API keys found
- Repo is archived/legacy — last meaningful code change was 2019; only CI/config updates since
- This is a 2019 educational/demo DoS script. Target is placeholder only. No live risk. Treat as archived.

## Next steps

None. Repo is healthy. Monitor future Dependabot PRs as they arrive.
