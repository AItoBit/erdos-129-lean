# Erdős Problem 129

Lean 4 proofs of the negative answer to [Erdős Problem 129](https://www.erdosproblems.com/129).
The definitions and proofs in `Erdos129.lean` were moved from
[formal-conjectures PR #6655](https://github.com/google-deepmind/formal-conjectures/pull/6655),
commit `7950d6f39eadea427345642eb76fd6b250a89e6f`.
The original Apache 2.0 license and attribution are preserved.

The main results are:

- `Erdos129.two_pow_lt_R`: for `100 ≤ n`, `2 ^ (n / 100) < R n 3 2`.
- `Erdos129.not_eventually_R_lt`: the proposed bound fails even eventually.
- `Erdos129.erdos_129`: the original statement has a negative answer.

The proof counts two-colourings using edge-disjoint triangles and a union bound.
A two-colour Ramsey argument shows the set defining `R n 3 2` is nonempty.
The definitions agree with those in the statement repository. The repository-specific
`answer(False)` notation is replaced here by `False`.

## Build

Uses Lean and Mathlib `v4.33.1`.

```sh
lake exe cache get
lake --wfail build
```

`Audit.lean` prints the axioms of all three main results.
