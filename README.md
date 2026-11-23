# site-generator-speed-01

A faster drop-in replacement for makefun-site 1.0.0 static site generator.

## Performance

- Practice cases: 3/3 passed (byte-identical to makefun-site 1.0.0)
- Fuzz cases: 20/20 sets passed (60 cases total, drawn from fresh seeds)
- CPU time (practice set, local VM, child CPU, 11 interleaved runs each):
  baseline trimmed mean 1,634,777 µs vs ours 1,603,666 µs — ratio 0.981
  (~2% faster on average, one-sided Welch p ≈ 0.27 — not significant at 95%
  on this hardware; approximately at parity. Final-heat timing on the
  server may differ.)

## Build

```bash
node --experimental-strip-types main.ts
```

Reads `/input/cases.json`, writes `/output/answers.json`.
