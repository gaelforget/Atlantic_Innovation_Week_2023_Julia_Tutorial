
# Characterizing Ocean Ecosystems using Sentinel-3 data with Julia

- Author : `Gaël Forget (MIT)`
- Event : `Atlantic Innovation Week 2023`
- Date : `2023/03/21`
- More Info : [AIW23](https://www.atlanticinnovationweek.org), [julia](https://julialang.org)

[![DOI](https://zenodo.org/badge/616272116.svg)](https://zenodo.org/badge/latestdoi/616272116)

Notebook is named [Sentinel-3\_first\_plot.jl](https://github.com/gaelforget/Atlantic_Innovation_Week_2023_Julia_Tutorial/blob/main/Sentinel-3_first_plot.jl) and hosted at [Sentinel-3\_first\_plot.html](https://gaelforget.github.io/Atlantic_Innovation_Week_2023_Julia_Tutorial/Sentinel-3_first_plot.html)

<img src="https://user-images.githubusercontent.com/20276764/226612244-8a0b955a-97e0-4e05-aa90-1857c721f6bd.png" width="300" height="120">

_Directions for using Julia and the notebook are provided below._

## 3. Interact With Notebooks

1. [Pluto](https://plutojl-preview.netlify.app) : provided
2. [Jupyter](https://jupyter.org) : DYI as exercise

### 3.1 Pluto

At the Julia prompt, run the following command.

```
using Pluto; Pluto.run(notebook="Sentinel-3_first_plot.jl")
```

This will open the notebook in your web browser via Pluto. First, let the notebook run. Once done, interact via the widgets or code cells.

### 3.2 Jupyter

At the Julia prompt, run the following command.

```using IJulia; notebook()```

This will start jupyter in your web browser. Start a new notebook, choose Julia as kernel, and then copy/paste [code from Pluto notebook](https://github.com/gaelforget/Atlantic_Innovation_Week_2023_Julia_Tutorial/blob/main/Sentinel-3_first_plot.jl)

## 2. Read Data and Visualize

Once you have completed the set-up (section 1 below) then try

```
include("Sentinel-3_first_plot.jl");
f
```

This should open a widow displaying a collection of data points.

## 1. Get Julia and Set-Up

- Download [Julia 1.9](https://julialang.org/downloads/#upcoming_release) and Start Julia ([go here for docs](https://julialang.org))
- Download this folder and copy its path
- Provide this path as `path0` (see below)
- Run commands below in Julia (type _return_ after each line).

```
path0="PASTE CORRECT PATH HERE"

cd(path0)
using Pkg
Pkg.activate(".")
Pkg.instantiate()
Pkg.status()
```

The final command should respond with something like

```
julia> Pkg.status()
Status `~/2023-AIW-Tutorial/Project.toml`
  [5ae59095] Colors v0.12.10
  [a93c6f00] DataFrames v1.5.0
  [5789e2e9] FileIO v1.16.0
  [e9467ef8] GLMakie v0.8.2
  [85f8d34a] NCDatasets v0.12.13
  [c3e4b0f8] Pluto v0.19.22
  [7f904dfe] PlutoUI v0.7.50
  [276b4fcb] WGLMakie v0.8.6
  [b77e0a4c] InteractiveUtils
  [d6f4376e] Markdown
  [10745b16] Statistics v1.9.0
```

_Note for Windows User : use double backslash in file paths, e.g., `cd("C:\\Users\\Joe\\Folder")`._
