# Illinois Browser Operating System Case Study

This repository contains our Illinois Browser Operating System (IBOS) Case Study.
This study focuses on verifying that two properties hold for IBOS:

- the same-origin policy (SOP)
- address bar correctnesss (ABC)

The reposistory also contains the complete source code of the IBOS specification
itself as well as our associated analysis tools and supporting proofs.
Aside from a few supporting shell scripts, all specifications, proofs, and tools
are written in [Maude](http://maude.cs.illinois.edu).
Since there are many pieces involved in this puzzle, we list them all here.

Included Specifications:

1. IBOS system specification as a rewrite theory - `systems/ibos.maude`
2. SOP/ABC property specifications as an equational theory - `tests/systems/ibos-preds.maude`

Automatic Analysis Tools:

1. Reachability Logic Tool (RLTool) - a universially quantified reachability claim theorem prover for rewrite theories - `rltool.maude`
2. Maude Termination Assistant (MTA) - a tool for proving that a rewrite theory is terminating using recursive path orderings or polynomial orderings - `mta/mta.maude`
3. Prototype Hierarchical Church-Rosser Checker Tool - a tool for checking the confluence of a theory hierarchically - `confluence.maude`
4. Prototype Variant Solveable Function Checker - a tool for checking when certain equalities have a complete set of unifiers in a finite variant property (FVP) subtheory - `partialfvp.maude`

Pen-and-Paper Analysis Tool:

1. Hierarchical Sufficient Completeness Checker - documented in Stephen Skeirik's thesis

Automated Proofs:

1. Reachability Proof of the SOP/ABC for IBOS (these were encoded together in a single proof) - `tests/systems/ibos-abc.maude`
2. Proof of termination of IBOS via MTA - `tests/tools/ibos-preds-term.maude`
3. Proof of confluence of IBOS via the prototype hierarchical confluence checker - `tests/tools/ibos-preds-confluence.maude`
4. Proof of variant solveability of selected equalities via the prototype variant sovleable function checker - `tests/systems/ibos-preds-pfvp.maude`

Pen-and-Paper Proofs:

1. Proof of sufficient completeness of IBOS via the sufficient completness checker - documented in Stephen Skeirik's thesis
