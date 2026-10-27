# Lesson 01 specification

## STUDIO-001 · Launch a tested calculator on an existing server

**Status:** Approved new deployment completed October 27, 2026; local checks and public verification passed. Learner interpretation, own-site observation and keep decision are recorded; summary accuracy/publication approval is recorded; GitHub completion remains pending.
**Next step:** Complete the PR/CI/merge workflow; SSH access and learner summary review are complete.
**Instructor implementation:** [issue #9](https://github.com/kaw393939/373_hosting/issues/9).
**Own lesson issue:** [STUDIO-001 #1](https://github.com/Y-Just-Y/373_hosting_dfp/issues/1), created after deployment to record the approved scope.

## Agreed result

Launch the supplied published calculator image through your existing Traefik
network and a nonconflicting HTTPS hostname. Preserve unrelated services and
host access. Do not add another proxy/updater or build a substitute image.
The [release selection](studio/calculator-release.json) supplies the expected
commit and multi-platform digest independently of the running website.
An explicitly agreed adoption of a matching existing deployment is recorded
as adoption, not a fresh launch. This bounded lesson does not certify the whole
server baseline or a vulnerability-free image.

- **Public hostname:** https://calc.lwdgyasteri.com.
- **New launch or adopted deployment, and reason:** New launch; no existing calculator route or lesson container was present. User approved the adapted deployment plan and execution.
- **Own issue / feature branch:** [Issue #1](https://github.com/Y-Just-Y/373_hosting_dfp/issues/1); branch `codex/studio-001-calculator`.
- **Agreed scope or actual access/configuration gap:** One pinned calculator on the existing edge network with a separate file-provider route using existing HTTPS. See [approved adaptation](studio/deployment-plan/README.md). GitHub SSH access is verified as Y-Just-Y. PR/CI remain pending.

Private SSH targets and configuration stay in ignored local state. Share only
reviewed, selected evidence; never commit credentials or raw server output.

## Evidence to keep

| Evidence | Actual result / link |
|---|---|
| Prepared Black/Pylint/pytest and real-image browser checks | Passed locally: Black, Pylint, 91 unit/integration tests and 2 Docker/Chromium E2E tests. CI pending. |
| Hosted image/commit, trusted HTTPS, valid and rejected API cases | Passed; [latest sanitized report](studio/evidence.json) and [initial new-launch report](studio/deployment-plan/initial-launch-evidence.json). |
| Preservation of unrelated services | Passed selected before/after checks: original containers/ports, original configuration hashes, HTTP-to-HTTPS behavior and homepage body hashes for production/QA. [Supplemental evidence](studio/deployment-plan/additional-evidence.json). |
| Own prediction, check interpretation, browser observation and keep/revise reason | [LEARNING.md](LEARNING.md): actual contributions and AI help recorded; accuracy/publication review approved October 27, 2026 |
| Accuracy review before publishing learner excerpts | Approved October 27, 2026; see LEARNING.md |
| Actual PR, latest CI, merge and issue closure | Pending |

Link the exported `studio/evidence.json`, actual CI and issue/PR when available.
CI does not deploy this server. A fixture, green check, timestamp, closed issue
or AI assertion alone does not establish the full result. `status` reports
recorded evidence and readiness for instructor review; it does not grade,
certify authorship or establish understanding.

## Optional instructor history

The records below are background, not steps to repeat. Their original anchors
remain here so earlier links continue to work.

## HOST-001 · Keep the Traefik dashboard private

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-001--keep-the-traefik-dashboard-private).

## HOST-002 · Controlled host maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-002--controlled-host-maintenance).

## HOST-003 · Companion image security maintenance

[Historical requirement and evidence](book/changes/hosting-spec-history.md#host-003--companion-image-security-maintenance).
