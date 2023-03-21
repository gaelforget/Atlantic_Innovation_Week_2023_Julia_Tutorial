
# Characterizing Ocean Ecosystems using Sentinel-3 data with Julia

- Author : `Gaël Forget (MIT)`
- Event : `Atlantic Innovation Week 2023`
- Date : `2023/03/21`
- More Info : [AIW23](https://www.atlanticinnovationweek.org), [julia](https://julialang.org)

The notebook is named [Sentinel-3\_first\_plot.jl](https://github.com/gaelforget/Atlantic_Innovation_Week_2023_Julia_Tutorial/blob/main/Sentinel-3_first_plot.jl) and hosted at [Sentinel-3\_first\_plot.html](https://gaelforget.github.io/Atlantic_Innovation_Week_2023_Julia_Tutorial/Sentinel-3_first_plot.html)

<img src="https://user-images.githubusercontent.com/20276764/226612244-8a0b955a-97e0-4e05-aa90-1857c721f6bd.png" width="300" height="120">

_Directions for using Julia and the notebook are provided below._

## 3. Interact With Notebooks

1. [Pluto](https://plutojl-preview.netlify.app) : provided
2. [Jupyter](https://jupyter.org) : DYI as exercise

!!! Tip 
    For jupyter, you can : open new notebook, choose Julia as kernel, and copy/paste code from Pluto notebook.

## 2. Read Data and Visualize

Once you have completed the set-up (section 1 below) then try

```
include("Sentinel-3_first_plot.jl");
f
```

This should open a widow displaying a collection of data points.

## 1. Get Julia and Set-Up

- Download and Start Julia ([go here](https://julialang.org/downloads/))
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

## Data

The data is downloaded from <https://dataspace.copernicus.eu> and the following samples used for this tutorial. 

This data was collected by `Sentinel-3B` for ocean color.

- `S3B_OL_2_WFR____20230318T064415_20230318T064715_20230318T085004_0180_077_191_3420_MAR_O_NR_003.SEN3/`
- `S3B_OL_2_WFR____20230319T142800_20230319T143100_20230319T163253_0179_077_210_2520_MAR_O_NR_003.SEN3/`
- `S3B_OL_2_WFR____20230319T210557_20230319T210857_20230319T230901_0179_077_214_2160_MAR_O_NR_003.SEN3/`

