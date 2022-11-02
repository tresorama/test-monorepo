# Test Monorepo

Every branch use a different monorepo strategy.
Check them out !

## What's included as workspaces ?

Workspaces are all subdirectory of `packages` and `apps`.

- `@tresorama-test-lib/generate-text-permutation`
- `@tresorama-test-lib/save-to-disk`

### @tresorama-test-lib/generate-text-permutation

#### When it's useful ??

When you need to generate a lot of combinations of strings to later analyze them and choose from.
The script generate the Cartesian Product of arrays of strings.

Example:

```ts
const input = [
  ["Mario", "Luigi", "Silvio"],
  ["gioca a pallone", "scrive una lettera", "salta la corda"],
  ["in cortile", "al bar", "in camera"],
];

const output = generateTextPermutation(input);

// output  =>
[
  "Mario gioca a pallone in cortile",
  "Mario gioca a pallone al bar",
  "Mario gioca a pallone in camera",
  "Mario scrive una lettera in cortile",
  "Mario scrive una lettera al bar",
  "Mario scrive una lettera in camera",
  "Mario salta la corda in cortile",
  "Mario salta la corda al bar",
  "Mario salta la corda in camera",
  "Luigi gioca a pallone in cortile",
  "Luigi gioca a pallone al bar",
  "Luigi gioca a pallone in camera",
  "Luigi scrive una lettera in cortile",
  "Luigi scrive una lettera al bar",
  "Luigi scrive una lettera in camera",
  "Luigi salta la corda in cortile",
  "Luigi salta la corda al bar",
  "Luigi salta la corda in camera",
  "Silvio gioca a pallone in cortile",
  "Silvio gioca a pallone al bar",
  "Silvio gioca a pallone in camera",
  "Silvio scrive una lettera in cortile",
  "Silvio scrive una lettera al bar",
  "Silvio scrive una lettera in camera",
  "Silvio salta la corda in cortile",
  "Silvio salta la corda al bar",
  "Silvio salta la corda in camera"
]
```
