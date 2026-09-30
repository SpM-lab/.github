# SpM-lab

Open-source tools for imaginary-time Green's functions in quantum many-body
physics: compact representations (intermediate representation, discrete
Lehmann representation, minimal pole representations), sparse sampling, and
analytic continuation.

## sparse-ir: start here

| You use | Library | Docs |
| --- | --- | --- |
| Python | [sparse-ir](https://github.com/SpM-lab/sparse-ir) (`pip install sparse-ir`) | [sparse-ir.readthedocs.io](https://sparse-ir.readthedocs.io) |
| Julia | [SparseIR.jl](https://github.com/SpM-lab/SparseIR.jl) (`] add SparseIR`) | [docs](https://spm-lab.github.io/SparseIR.jl/dev/) |
| Rust, C, Fortran | [sparse-ir-rs](https://github.com/SpM-lab/sparse-ir-rs) (`sparse-ir`, `sparse-ir-capi` on crates.io) | [Rust guide](https://spm-lab.github.io/sparse-ir-rs/) |

- **Tutorials** (Python and Julia notebooks): [sparse-ir-tutorial-v2](https://spm-lab.github.io/sparse-ir-tutorial-v2/)
- **Theory and notation** across languages: [sparse-ir-doc](https://spm-lab.github.io/sparse-ir-doc/)

sparse-ir-rs is the shared backend: its C API is what sparse-ir (via
`pylibsparseir`) and SparseIR.jl (via `libsparseir_jll`) call, and it ships
the Fortran bindings.
New features land there first: the DLR built without an IR basis and
ESPRIT/MiniPole pole extraction are currently on the `main` branch of
sparse-ir-rs only, not yet in a release or in the Python and Julia libraries.

## Analytic continuation

- [SpM](https://github.com/SpM-lab/SpM) — sparse modeling analytic continuation (C++)
- [pySpMAC](https://github.com/SpM-lab/pySpMAC) — sparse modeling analytic continuation (Python)
- [admmsolver](https://github.com/SpM-lab/admmsolver) — a general ADMM solver (Python)
- [Nevanlinna.jl](https://github.com/SpM-lab/Nevanlinna.jl) — Nevanlinna analytic continuation (Julia)

## Older repositories

These are superseded and kept for reference:

| Repository | Use instead |
| --- | --- |
| irbasis, irlib | sparse-ir, SparseIR.jl |
| SparseIR_deprecated.jl | SparseIR.jl |
| libsparseir, pysparseir, LibSparseIR.jl | sparse-ir-rs |
| sparse-ir-fortran | `fortran/` in sparse-ir-rs |
| sparse-ir-tutorial, sparse-ir-tutorial-v1 | sparse-ir-tutorial-v2 |

## Issues that span several projects

Open them in [SpM-lab/.github](https://github.com/SpM-lab/.github/issues).
Issues about a single library belong in that library's repository.
