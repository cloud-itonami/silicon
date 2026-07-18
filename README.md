# silicon 珪

Ternary silicon-fab orchestration actor for lithography, wafer processing, chip test,
packaging, process simulation, wafer handling, and append-only lot traceability.

Canonical metadata, schema, seed, and migration records are EDN. Shared AT Protocol lexicons
remain centrally governed under `00-contracts/lexicons/com/etzhayyim/silicon/`; JSON belongs
only at external wire boundaries.

## Test

```bash
clojure -M:test -m silicon.test-runner
```

The implementation is deterministic R0 design/simulation code. Real equipment dispatch remains
Council-gated, and the actor holds no platform or member signing key.
