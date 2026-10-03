# Beamo Flasher release assets — agent guide

`AGENTS.md` is the sole guide for all agents.

This repository holds public installer, updater and image assets; application
source belongs to Beamo Flasher. Read [README.md](README.md) and the source
project's release runbook before changing distribution metadata.

## CI, cost and documentation

Read `~/dev/AGENTS.md` for shared checkout, cost, documentation and storage rules.

- Iterate locally; run the applicable full local gate before release. Hosted
  CI is only for necessary final public/customer production verification,
  never routine work, draft PRs, previews or unshipped instruction/doc maintenance. Local
  scripts named `ci` remain local; do not push merely to trigger CI.
- Run the fewest required hosted jobs. Reuse only evidence for the exact final
  SHA, artifacts and config; revalidate after changes. Fix every candidate/gate
  failure and material warning, then rerun until all applicable checks pass.
  Pending, canceled, blocked, timed out and unexpected skips are not passes;
  path skips require workflow evidence. Never weaken tests/coverage or retry blindly.
- Check automatic triggers and gate publication on successful verification.
  Preserve required statuses, branch protection, scheduled security/ops checks,
  native acceptance and approvals; record proof and verify after deployment.
  No hosted CI means retain local/manual gates. Changes to automation or
  publication need task authority. Avoid duplicate providers/runs.

**Project gate:** Before public asset/updater publication, require Beamo Flasher's successful
final source/native/artifact qualification and match its receipts to these
exact bytes. Reuse that source proof rather than rebuilding or inventing CI in
this assets repository. Metadata/checksum/updater verification and hashing
published downloads remain necessary; preserve explicit release approval.

## Release integrity

Preserve asset names, source identity, checksums, signatures and updater contracts.
Release publication or replacement needs explicit authorization and successful
platform validation. Download and hash published bytes before claiming success.
Use existing verification scripts/configuration; do not invent a test gate.
Never commit binaries, credentials or disposable staging as documentation.
Preserve unrelated work and stage only explicit owned paths.
