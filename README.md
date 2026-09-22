# Superconductivity: From BCS Theory to Bose-Einstein Condensation of Pairs

A 77-page report tracing superconductivity from its phenomenological description through
its microscopic origin to its macroscopic field theory, written for the course of **Methods
and Models for Statistical Mechanics** (Engineering Physics, Politecnico di Milano,
2025/26).

The thread running through it is a single question — *what is actually condensing, and how
do we describe it at each scale?* — asked five times, each chapter answering the one the
previous left open.

📄 **[Read the report](Superconductivity_BCS_to_BEC.pdf)**

## Why this is here

Superconducting qubits are the dominant platform in quantum computing, and they are built
on exactly this physics: the Josephson junction, the transmon's charging and Josephson
energies, and the protection the superconducting gap provides against quasiparticle
poisoning all rest on Cooper pairing, the macroscopic phase of the condensate, and the
Ginzburg-Landau description of how that phase responds to fields.

This report covers those foundations rather than the devices built on them.

## Contents

**1 — Superconductivity.** Zero resistivity and the Meissner-Ochsenfeld effect as the two
defining experimental features, and why a superconductor is not simply a perfect conductor.
The London equations, derived from the vanishing of the canonical momentum in the
condensate, and the penetration depth λ_L that follows.

**2 — BCS theory.** The phonon-mediated attraction, and the Cooper problem solved twice:
first in vacuum, where a bound state requires the attraction to exceed a finite threshold
V₀,min, then inside a filled Fermi sea, where an arbitrarily weak attraction suffices. The
contrast between the two calculations is the whole content of the Cooper instability.
Closes with the BCS ground state as a coherent superposition of occupied and empty pair
states.

**3 — Bose-Einstein condensation.** The Bose-Einstein distribution, the critical density and
the condensate fraction, then the dimensionality question: why condensation fails in one and
two dimensions for quadratic dispersion, and the general criterion d/s > 1. Ends with the
order parameter and the spontaneous breaking of U(1) phase symmetry.

**4 — Superconductivity as a BEC of pairs.** The BCS-BEC crossover. In the weak-coupling
limit Pauli blocking makes the pair dispersion approximately linear rather than quadratic,
which restores a finite critical temperature in quasi-two-dimensional systems. The
divergence of T_c for hypothetically unbreakable pairs, and how a finite pair-breakup
momentum regularises it.

**5 — Landau-Ginzburg formalism.** Landau's free-energy expansion, the GL functional with
minimal coupling to the electromagnetic field, and the two GL equations obtained
variationally. The coherence length ξ, the recovery of the London penetration depth from
the GL order parameter, and the classification into Type I and Type II through κ = λ/ξ.

**Appendices A-E** carry the full derivations for each chapter, kept out of the main text so
the argument stays readable: the London equation solutions, the Cooper integral equation,
the 3D density of states and the Gamma-zeta integrals, the generalised critical temperature,
and the variational derivation of both Ginzburg-Landau equations.

## Sources

The full LaTeX sources are in [`src/`](src/), built on the official Politecnico di Milano
thesis class:

```
src/
├── main.tex                  # document root — chapter order is set here
├── References.bib
├── Abstract/
├── Chapters/                 # one folder per chapter, each with its own Images/
├── Appendix/
├── Configuration_Files/      # PoliMi3i_thesis.cls and config.tex
└── Images/                   # institutional logos used by the title page
```

Note that the chapter *folder* numbering does not follow the order of the document: the
sequence is the one declared by the `\input` commands in `main.tex`.

To build:

```bash
cd src
latexmk -pdf main.tex
```

Requires a standard TeX distribution. The class file is included, so no separate template
installation is needed.

## Corrections

These are the notes of a student working through the material. If you find an error —
including a trivial one — open an issue. I would rather know.

## License

[CC BY-NC-ND 4.0](LICENSE). You may read, share and cite this work with attribution. You may
not use it commercially or distribute modified versions. Figures marked *"Image adapted
from"* are reproduced from the sources cited in the bibliography and remain the property of
their respective copyright holders; the same applies to the Politecnico di Milano marks in
`src/Images/`.

## Citation

```bibtex
@misc{fumagalli2026superconductivity,
  author       = {Marco Fumagalli},
  title        = {Superconductivity: From {BCS} Theory to {B}ose-{E}instein Condensation of Pairs},
  year         = {2026},
  howpublished = {Course report, Politecnico di Milano},
  url          = {https://github.com/marco992233/Superconductivity-bcs-to-bec}
}
```

---

Marco Fumagalli · [marco24.fumagalli@mail.polimi.it](mailto:marco24.fumagalli@mail.polimi.it) · [LinkedIn](https://www.linkedin.com/in/marco-fumagalli-70007924b/)
