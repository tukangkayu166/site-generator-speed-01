# site-generator-speed-01

[![make.fun](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/tukangkayu166/site-generator-speed-01/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/tukangkayu166/site-generator-speed-01/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122)

A faster drop-in replacement for makefun-site 1.0.0 static site generator. Entry for the [make.fun competition "Build a static site faster, 22 November 2026"](https://make.fun/bounty/site-generator-speed-01-run-20261122).

## Performance

- Practice cases: 3/3 passed (byte-identical to makefun-site 1.0.0)
- Fuzz cases: 20/20 sets passed (60 cases total, drawn from fresh seeds)
- grade-local: 3/3 passed
- CPU time (practice set, local VM, child CPU, 11 interleaved runs each, trimmed mean):
  baseline 1,304,463 µs vs ours 990,146 µs — ratio 0.7590 (1.317× speedup,
  one-sided Welch p ≈ 0.0000; a second run agreed at ratio 0.7620, p ≈ 0.0000).
  Beats the house baseline at >99.9% confidence on this hardware; final-heat
  timing on the server may differ.

## Build

```bash
node --experimental-strip-types main.ts
```

Reads `/input/cases.json`, writes `/output/answers.json`.
