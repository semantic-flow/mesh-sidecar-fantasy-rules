# mesh-sidecar-fantasy-rules

`mesh-sidecar-fantasy-rules` is the docs-rooted sidecar fixture repository for the Fantasy Rules Semantic Flow ladder.

For sidecar fixtures, `main` should ultimately look like the final generated mesh state: authored source files stay at the repository root, while generated Semantic Flow mesh output lives under `docs/`. During replay work, the cleaned setup state is carried by `a.00-blank-slate`; that branch contains deterministic replay assets under `.assets/` plus small repository-control files, but no generated mesh output.

Current replay branch prefix:

- `a.00-blank-slate`
- `a.01-source-only`
- `a.02-sidecar-mesh-created`
- later `a.*` rungs as the generator replays the ladder

The older unprefixed numbered branches are legacy fixture output. They may remain useful for comparison while the `a.*` chain is brought up, but they are not the source of truth for new regeneration work.

Source ownership:

- Accord manifests live in the Semantic Flow Framework conformance example.
- Replay source bytes live in this repository under `.assets/`.
- `a.00-blank-slate` is the replay base/control rung.
- Generated rung branch contents are disposable replay output.
- After the sidecar ladder is replayed and reviewed, the final generated rung can be merged back to `main`.

Regeneration is local-only by default in Weave's fixture ladder tool; pushing branch updates is an explicit follow-up step.
