# Mento V3 Shadow Audit Package

This repository packages the two public source repositories and exact commits used for Cantina's publicly available Mento V3 competition.

It is provided for yBorg participants during the yBorg program as a shadow audit for calibrating, testing, and regression-testing the security tools they are building.

## Included

- `sources/mento-core` — Mento V3 core contracts at the contest commit.
- `sources/bold` — Mento's BOLD/CDP contracts at the contest commit.
- `SOURCES.md` — provenance, commit hashes, and public source links.

## Clone

Both codebases are pinned Git submodules. Clone recursively so the exact contest sources and their pinned dependencies are checked out:

```sh
git clone --recurse-submodules https://github.com/yAudit/yborg-mento-v3-shadow-audit.git
cd yborg-mento-v3-shadow-audit
```

If the repository was cloned without submodules:

```sh
git submodule update --init --recursive
```

## Build

The projects retain their upstream build systems and instructions:

```sh
cd sources/mento-core
forge build
```

```sh
cd sources/bold/contracts
forge build
```

Dependencies are intentionally pinned by the upstream repositories' own submodule commits. No dependency versions have been updated for this package.

## Benchmark use

Run the tool against one or both source directories and preserve its raw output for later evaluation.

This package is for benchmarking and education. It is not a new audit, an endorsement of any tool, or a statement that the historical code is safe to deploy.
