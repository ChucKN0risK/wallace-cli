# Wallace

Analyze your CSS from the CLI, like [Parker](https://www.npmjs.com/package/parker) or [Stylestats](https://www.npmjs.com/package/stylestats)

## Usage

```sh
Usage
  $ wallace https://projectwallace.com

  Options
  --format, -f Format pretty (default) or JSON
  --compact, -c Show a compact output

  Examples
  $ wallace https://projectwallace.com
  $ wallace 'body { color: red; }'
  $ echo 'html { font-size: 16px; } | wallace
  $ wallace 'html {}' --format=json
  $ cat style.css | wallace --compact
```

## Output

```sh
┌────────────────────────────────────────────┐
│ Global                                     │
├─────────────────────────┬───────┬──────────┤
│ Stylesheet size         │ 41 B  │          │
├─────────────────────────┼───────┤          │
│ Simplicity              │ 1.000 │          │
├─────────────────────────┼───────┤          │
│ Cohesion                │ 3.000 │          │
├─────────────────────────┼───────┤          │
│ Rules                   │ 1     │          │
├─────────────────────────┼───────┼──────────┤
│ At-Rules                │ Total │ Unique   │
├─────────────────────────┼───────┼──────────┤
│ @media queries          │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ @font-faces             │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ @keyframes              │ 0     │ 0        │
├─────────────────────────┼───────┴──────────┤
│ @media queries          │ N\A              │
├─────────────────────────┼───────┬──────────┤
│ Selectors               │ Total │ Unique   │
├─────────────────────────┼───────┼──────────┤
│ All                     │ 1     │ 1        │
├─────────────────────────┼───────┼──────────┤
│ ID                      │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ JS                      │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ Universal               │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ Accessibility           │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ Average identifiers     │ 1.000 │          │
├─────────────────────────┼───────┴──────────┤
│ Max. identifiers        │ 1. body          │
├─────────────────────────┼──────────────────┤
│ Top specificity         │ 1. body          │
├─────────────────────────┼──────────────────┤
│ ID Selectors            │ N\A              │
├─────────────────────────┼──────────────────┤
│ JS Selectors            │ N\A              │
├─────────────────────────┼──────────────────┤
│ Universal Selectors     │ N\A              │
├─────────────────────────┼──────────────────┤
│ Accessibility Selectors │ N\A              │
├─────────────────────────┼───────┬──────────┤
│ Declarations            │ Total │ Share    │
├─────────────────────────┼───────┼──────────┤
│ Total                   │ 3     │          │
├─────────────────────────┼───────┼──────────┤
│ Unique                  │ 3     │ 100.000% │
├─────────────────────────┼───────┼──────────┤
│ !importants             │ 0     │ 0.000%   │
├─────────────────────────┼───────┼──────────┤
│ Properties              │ Total │ Share    │
├─────────────────────────┼───────┼──────────┤
│ All                     │ 3     │          │
├─────────────────────────┼───────┼──────────┤
│ Unique                  │ 3     │ 100.000% │
├─────────────────────────┼───────┼──────────┤
│ Prefixed                │ 0     │ 0.000%   │
├─────────────────────────┼───────┴──────────┤
│ Prefixed                │ N\A              │
├─────────────────────────┼───────┬──────────┤
│ Values                  │ Total │ Unique   │
├─────────────────────────┼───────┼──────────┤
│ Prefixed                │ 0     │ 0        │
├─────────────────────────┼───────┼──────────┤
│ Colors                  │ 1     │ 1        │
├─────────────────────────┼───────┼──────────┤
│ Font-sizes              │ 1     │ 1        │
├─────────────────────────┼───────┼──────────┤
│ Font-families           │ 0     │ 0        │
├─────────────────────────┼───────┴──────────┤
│ Unique Colors           │   1 × blue       │
├─────────────────────────┼──────────────────┤
│ Unique font-sizes       │  1 × 10px        │
├─────────────────────────┼──────────────────┤
│ Unique font-families    │ N\A              │
├─────────────────────────┼──────────────────┤
│ Prefixed                │ N\A              │
└─────────────────────────┴──────────────────┘
```

## Related

- [CSS Analyzer](https://github.com/projectwallace/css-analyzer) - The analyzer that powers this module
- [Gromit](https://github.com/bartveneman/gromit) - A test framework to assert that CSS doesn't exceeds certain tresholds.
- [CSS Analyzer Diff](https://github.com/bartveneman/css-analyzer-diff) - Calculates the diff between two sets of CSS analysis
