[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

# Learning Symbolic Expressions: Mixed-Integer Formulations, Cuts, and Heuristics,

This archive is distributed in association with the [INFORMS Journal on
Computing](https://pubsonline.informs.org/journal/ijoc) under the [GNU GPLv3](LICENSE).

The software and data in this repository are a snapshot of the software and data
that were used in the research reported on in the paper 
[Learning Symbolic Expressions: Mixed-Integer Formulations, Cuts, and Heuristics](https://doi.org/10.1287/ijoc.2022.0050) by Jongeun Kim, Sven Leyffer, Prasanna Balaprakash.
The snapshot is based on 
[this SHA](https://github.com/tkralphs/JoCTemplate/commit/f7f30c63adbcb0811e5a133e1def696b74f3ba15) 
in the development repository. 

## Cite

To cite the contents of this repository, please cite both the paper and this repo, using their respective DOIs.

https://doi.org/10.1287/ijoc.2022.0050

https://doi.org/10.1287/ijoc.2022.0050.cd

Below is the BibTex for citing this snapshot of the respoitory.

```
@article{Goyal2023decision,
  author =        { Kim, Jongeun and Leyffer, Sven and Balaprakash, Prasanna },
  publisher =     {INFORMS Journal on Computing},
  title =         {{Learning Symbolic Expressions: Mixed-Integer Formulations, Cuts, and Heuristics}},
  year =          {2023},
  doi =           {10.1287/ijoc.2019.2022.0050.cd},
  note =          {Available for download at https://github.com/INFORMSJoC/2022.0050},
}  
```

## Content

This repository contains MINLP-based symbolic regression algorithms in Julia, as well as the associated datasets.

## Install

The below instruction guides you how to install the requirements and run the code.

Install Julia. Available at [Julia Download](https://julialang.org/downloads/). This code is compatible with Julia 1.5.3.

Install SCIPOptSuite. Available at [SCIPOptSuite Download](https://www.scipopt.org/index.php#download). 
Before you download, please check which version is supported by the SCIP package in Julia [SCIP.jl News](https://github.com/scipopt/SCIP.jl/blob/master/NEWS.md).
The most recent version SCIP v.7.0.2 is supported (confirmed on 02/04/2021).

Execute `install_pkgs.jl` to install the required julia packages.

## Running an example

`scripts/example/data.txt` is a sample dataset. The formula is x1*x2+1. Each row represents a data point. The code assumes that the last column is the dependent varaible.

`scripts/main_example.jl` is an example code to run MINLP and STreCH. 

Once MINLP or STreCH is finished, it will create `df_sol.csv`, which includes the list of formulas and their objective values (MSE).

## Dataset used in the paper

`data/` contains all the datasets used in the paper. Each folder in `data/` includes a info file `info.txt`, two training set with/without noise, one validation set, and one testing set.


********************************************************************************

Notice: This software was developed in the course of or under prime
contract No. DE-AC02-06CH11357 between the U.S.
Department of Energy and UChicago Argonne, LLC.
This source code is licensed under the BSD-style license found in the `LICENSE` file in the root directory of this source tree.  
