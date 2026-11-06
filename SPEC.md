# Lesson 01 specification

## STUDIO-001 · Launch a tested calculator on an existing server

**Status:** Pending learner scope agreement and actual evidence.
**Next step:** Confirm your clone with the coach, then follow [Lesson 01](studio/lesson-01.md).
**Instructor implementation:** [issue #9](https://github.com/kaw393939/373_hosting/issues/9).
Create your own issue from the [lesson template](.github/ISSUE_TEMPLATE/studio-calculator.md).

## Agreed result

Launch the supplied published calculator image through your existing Traefik
network and a nonconflicting HTTPS hostname. Preserve unrelated services and
host access. Do not add another proxy/updater or build a substitute image.
The [release selection](studio/calculator-release.json) supplies the expected
commit and multi-platform digest independently of the running website.
An explicitly agreed adoption of a matching existing deployment is recorded
as adoption, not a fresh launch. This bounded lesson does not certify the whole
server baseline or a vulnerability-free image.

- **Public hostname:** https://calc.anncarlos.me
- **New launch or adopted deployment, and reason:** Adopted an existing deployment (not a new launch). Reason, in my words: "i would adopt the existing calculator because it is less risky since there are fewer steps". The supplied image was already running behind my Traefik before the studio tool was run; `launch` and `verify` recorded `adopted-existing`, `new_launch: false`.
- **Own issue / feature branch:** [issue #1](https://github.com/apink634/my-server-studio/issues/1); branch `studio-001-calculator`.
- **Agreed scope or actual access/configuration gap:** Run the supplied calculator image behind my existing Traefik and keep my existing sites working. My original droplet was deleted by mistake and rebuilt on 2026-11-04 on a replacement droplet (167.172.158.254); the instructor confirmed by email that a replacement droplet is fine.

Private SSH targets and configuration stay in ignored local state. Share only
reviewed, selected evidence; never commit credentials or raw server output.

## Evidence to keep

| Evidence | Actual result / link |
|---|---|
| Prepared Black/Pylint/pytest and real-image browser checks | Black passed. Pylint and pytest failed locally on Windows (os.geteuid, os.chown, signal.SIGHUP do not exist on Windows). Full local E2E not run (no local Docker). CI result: pending, see PR. |
| Hosted image/commit, trusted HTTPS, valid and rejected API cases | Verified 2026-11-05 about 7:05 PM Eastern: commit 4600202b…, trusted HTTPS, 6x7=42 (200), divide by zero (400), numeric string (422). See [studio/evidence.json](studio/evidence.json). |
| Preservation of unrelated services | `verify` preservation check: 5 items unchanged (container identity, state, published ports). My three Apache sites also passed `verify.py` on the server. |
| Own prediction, check interpretation, browser observation and keep/revise reason | [LEARNING.md](LEARNING.md), Pending; disclose assistance |
| Accuracy review before publishing learner excerpts | Pending |
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
