# Mint Releases

Public distribution repo for [Mint](https://github.com/makenode-vn/monorepo) desktop app
binaries and the `tauri-plugin-updater` manifest (`latest.json`).

**No source code lives here — this repo only exists so Mint's auto-updater has somewhere
public to fetch from.** Mint's source repo is private, and GitHub Release assets on a
private repo return `404` to an unauthenticated request (verified directly). An installed
copy of Mint, running on a user's machine with no GitHub credentials, can only ever check
for updates against a public repo — hence this one. See
[ADR-007](https://github.com/makenode-vn/monorepo/blob/main/mint/docs/decisions/adr-007-ci-cd.md#update-2026-09-19-auto-update-windows--macos)
in the source repo for the full design, and
[`releasing.md`](https://github.com/makenode-vn/monorepo/blob/main/mint/docs/releasing.md)
for the practical steps to cut a release.

## What's here

- **Releases tagged `vX.Y.Z`** (from `mint-release.yml`, triggered by pushing the source
  repo's `release` branch) — the **stable** channel. Published as drafts first; a human
  reviews and publishes.
- **One release tagged `beta`** (from `mint-release-beta.yml`, manually triggered) — the
  **beta / internal testing** channel. Always replaced in place on the next beta build, so
  its manifest URL never changes.

Each release carries, per platform, the installer/bundle plus a `.sig` file (minisign
signature) and a shared `latest.json` manifest that `tauri-plugin-updater` reads.

## Don't

- Don't create or edit releases here by hand — CI owns this repo's releases. A manual
  release with a mismatched `latest.json` shape will make the updater silently reject it.
- Don't delete old stable releases — a user on a bad build may need to manually download
  and reinstall the previous one (see ADR-007's rollback section).
