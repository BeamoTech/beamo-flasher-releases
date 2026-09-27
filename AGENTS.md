# Beamo Flasher release assets — agent guide

`AGENTS.md` is the sole project instruction file for all coding agents.

This repository holds public installer, updater and image assets; application
source belongs to Beamo Flasher. Read [README.md](README.md) and the source
project's release runbook before changing distribution metadata.

## CI, cost and documentation

- Use **Blacksmith** runners for supported GitHub Actions CI. Check the current
  [runner documentation](https://docs.blacksmith.sh/blacksmith-runners/overview)
  and repository access before selecting labels. Preserve required checks and
  native platform coverage; retain an existing gate until its replacement proves
  equivalent coverage for the same source. Record any provider exception.
- Minimize total cost across CI, hosting, storage, network, APIs, AI and tooling.
  Choose the least costly option that meets the task's quality, security,
  reliability and performance requirements. Preserve mandated models and gates;
  never trade away correctness, coverage, accessibility or data safety for price.
- Use the fewest hosted CI runs that still cover changed paths, scheduled
  checks and required gates. Iterate locally, route jobs by scope, reuse valid
  caches, avoid duplicate runs and bound retries/concurrency. Cancel superseded
  verification when safe; review releases and migrations before cancellation.
  Preserve checks for the exact commit and native platforms. Measure usage, expire disposable
  artifacts and retire only verified idle resources within task authority.
- Keep Markdown focused: one canonical home per topic, short sections and useful
  links. Keep commands and safeguards near their use; move detailed history to
  dated evidence. Update stale guidance against code, preserve release records,
  and avoid duplicating this policy in every document.

## Release integrity

Preserve asset names, source identity, checksums, signatures and updater contracts.
Release publication or replacement needs explicit authorization and successful
platform validation. Download and hash published bytes before claiming success.
Use existing verification scripts/configuration; do not invent a test gate.
Never commit binaries, credentials or disposable staging as documentation.
Preserve unrelated work and stage only explicit owned paths.
