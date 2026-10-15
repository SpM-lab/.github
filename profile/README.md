# SpM-lab

Open-source tools for imaginary-time Green's functions in quantum many-body
physics: compact representations (intermediate representation, discrete
Lehmann representation, minimal pole representations), sparse sampling, and
analytic continuation.

**Website: [spm-lab.github.io](https://spm-lab.github.io/)**, the entry point
to everything below.

## sparse-ir ecosystem

Start at the **[sparse-ir documentation](https://spm-lab.github.io/sparse-ir-doc/)**:
an overview, the [history and comparison of IR, DLR and MiniPole](https://spm-lab.github.io/sparse-ir-doc/src/history_comparison.html),
the [shared notation](https://spm-lab.github.io/sparse-ir-doc/src/notation.html),
and a guide to the libraries.

| You use | Library | Docs |
| --- | --- | --- |
| Python | [sparse-ir](https://github.com/SpM-lab/sparse-ir) (`pip install sparse-ir`) | [sparse-ir.readthedocs.io](https://sparse-ir.readthedocs.io) |
| Julia | [SparseIR.jl](https://github.com/SpM-lab/SparseIR.jl) (`] add SparseIR`) | [docs](https://spm-lab.github.io/SparseIR.jl/stable/) |
| Rust, C, Fortran | [sparse-ir-rs](https://github.com/SpM-lab/sparse-ir-rs) (`sparse-ir`, `sparse-ir-capi` on crates.io) | [Rust guide](https://spm-lab.github.io/sparse-ir-rs/) |

- **Tutorial** (Python and Julia notebooks): [sparse-ir-tutorial](https://spm-lab.github.io/sparse-ir-tutorial/)

sparse-ir-rs is the shared backend: its C API is what sparse-ir (via
`pylibsparseir`) and SparseIR.jl (via `libsparseir_jll`) call, and it ships
the Fortran bindings. New features, such as MiniPole/ESPRIT and the DLR built
without an IR basis, land there first.

## Analytic continuation

- [SpM](https://github.com/SpM-lab/SpM) — sparse modeling analytic continuation (C++)
- [pySpMAC](https://github.com/SpM-lab/pySpMAC) — sparse modeling analytic continuation (Python)
- [admmsolver](https://github.com/SpM-lab/admmsolver) — a general ADMM solver (Python)
- [Nevanlinna.jl](https://github.com/SpM-lab/Nevanlinna.jl) — Nevanlinna analytic continuation (Julia)
- [MiniPole](https://spm-lab.github.io/sparse-ir-rs/tutorials/minipole.html) — minimal pole representation, in sparse-ir-rs

## Older repositories

These are superseded and kept for reference:

| Repository | Use instead |
| --- | --- |
| irbasis, irlib | sparse-ir, SparseIR.jl |
| SparseIR_deprecated.jl | SparseIR.jl |
| libsparseir, pysparseir, LibSparseIR.jl | sparse-ir-rs |
| sparse-ir-fortran | `fortran/` in sparse-ir-rs |
| sparse-ir-tutorial-v1 (archived) | sparse-ir-tutorial |

## Issues that span several projects

Open them in [SpM-lab/.github](https://github.com/SpM-lab/.github/issues).
Issues about a single library belong in that library's repository.
