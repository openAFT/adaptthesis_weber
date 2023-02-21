* _University:_ **University of Zurich ([UZH])**
* _Department:_ **Department of Physics**
* _Supervisor:_ **Prof. Jan Unkelbach**
* _Time:_ **June 2022 - March 2023**

This repository contains the source code for the Master Thesis of Janic Tom Weber.


## Requirements

To compile this thesis, one needs a TeX Live 2022 distribution. All figures in the thesis are compiled using scripts that are contained in this repository. This means, having installed the `adpatfx` and `adapsim` package, one can recreate all plots. The `adpatfx` package installs dependency automatically needed for plotting. For Python version 3.10 or later is necessary. Ideally one has also created a virtual environment. So in summary:

1. TeX Live 2022
2. Python 3.10 or Later
3. `adaptfx` and `adapsim` package


## Reproduce

If you want to reproduce the thesis, i.e. recompile it and recreate all the figures, do the following (ideally inside a virtual environment, like `venv`):

First, install the dependencies from [adaptfx](https://github.com/openAFT/adaptfx) and [adaptsim](https://github.com/openAFT/adaptsim)

With the CLI of `adapsim` run
```
$ ast -f graphics/*.json
```

And after this, you can build the entire document by running
```
$ latexmk -bibtex -f -logfilewarnings -nobibfudge -outdir=./_build -pdf ada.tex
```