# modsoc_Julia
This repository contains Julia Jupyter notebooks that reimplement the NetLogo models from *Modeling Social Behavior: Mathematical and Computational Models of Social Dynamics and Cultural Evolution* by Paul E. Smaldino. The original NetLogo code is available at: https://github.com/psmaldino/modsoc

Notebooks are organized by chapter. Files with the _GUI tag provide interactive visualizations akin to NetLogo; files without _GUI focus on parameter sweeps and reproducing plots from the book. The models are implemented primarily with Agents.jl: https://juliadynamics.github.io/Agents.jl/stable/

A few notebooks include extensions beyond the book: `SIR.ipynb` adds additional plotting/analysis, `SIMPLE.ipynb` includes a cluster-size analysis, and `P_BC_NBC_GUI.ipynb` uses a custom GUI configuration. In Chapters 6 and 7, the code also includes a switch to toggle synchronous vs asynchronous interactions.

Some notebooks also consolidate multiple NetLogo model variants into a single file, for example, SI_SIS_SIR_GUI.ipynb bundles the SI/SIS/SIR models, and P_BC_NBC.ipynb combines the P (positive interactions), BC (bounded confidence), and NBC (negative interactions with bounded confidence) variants.

Install packages used across notebooks (thank you to the developers for these superb packages):
```julia
using Pkg
Pkg.add([
  "Agents","Plots","ProgressMeter","Distributions","StatsBase","Graphs",
  "StaticArrays","Colors","ColorSchemes","LaTeXStrings","Measures",
  "GLMakie","GraphRecipes","Observables","OrderedCollections"
])
``` 

For questions, comments, or suggestions, please contact `bfried@ucmerced.edu` with subject line `modsoc_Julia`.


If you'd like to cite this repository, you can do so using: 
[![DOI](https://zenodo.org/badge/1154952499.svg)](https://doi.org/10.5281/zenodo.18730422)

