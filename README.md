# fit_target2cavity

find chemical(s) fitting a given cavity, using mol2vec and cavity vectors

## installing required packages

After [installing julia](https://julialang.org/downloads/), you need to run the following to start using the scripts

```bash
git clone
cd fit_target2cavity
julia 
```

## training

run the following command

```bash
julia training.jl cavity.csv ligands.csv
```

command will save trained model in current directory after training is complete

## predictions

for a given cavity, and trained model, you can get **closest** chemical vector by running the following command

```bash
julia predict.jl test.csv model
```

## cavity vectors

you need to install and run [IChem software](http://bioinfo-pharma.u-strasbg.fr/labwebsite/download.html) to extract cavity vectors from pdb file of your target protein

```bash
IChem pdbconvert target.pdb
IChem volsite target.pdb
```
