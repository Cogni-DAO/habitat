# node-template

Node-at-root template for a **Cogni full-app submodule node** — the canonical single node, minted via GitHub generate-from-template and added as a git submodule at `nodes/<slug>/` in the operator monorepo (`Cogni-DAO/cogni`).

Seeded from `Cogni-DAO/cogni:nodes/node-template/` @ `229d85d40` (2026-06-04).

- **Node-at-root** layout (`app/`, `graphs/`, `k8s/`, `packages/`, `.cogni/`) so it mounts cleanly at `nodes/<slug>/` when added as a submodule.
- `.cogni/secrets-catalog.yaml` + `k8s/external-secrets/` are intentionally absent (bug.5086 Part D: a node inherits baseline secrets via the substrate; declares its own only when it has unique ones).
- Standalone root scaffold (own `ci.yaml`/biome/tsconfig/`package.json`) and the catalog-driven sync are follow-on — see `Cogni-DAO/cogni` `docs/spec/node-ci-cd-contract.md` §Submodule-pinned nodes.

> WIP — not yet a GitHub template repo; populated as the submodule-birth rails are proven (no node minted from it until then).
