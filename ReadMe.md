# Bicriterion assignment and multi modal assignment problems

This is an example on how an readme file can look, see [this file](https://github.com/MCDMSociety/MOrepo/blob/master/contribute.md) for info about how to contribute.

The paper consider 10 instances for the classical bi-objective linear assignment problem. 

## How to cite

To cite the paper use

```
@ARTICLE{Pedersen08,
   Author = {Pedersen, C.R. and Nielsen, L.R. and Andersen, K.A.},
   Title = {The Bicriterion Multi Modal Assignment Problem: Introduction, Analysis, and Experimental Results},
   Year = {2008},
   Volume = {20},
   Number = {3},
   Journal = {Informs Journal on Computing},
   Institution = {Department of Operations Research, University of Aarhus},
   School = {Department of Operations Research, University of Aarhus},
   Pages = {400–-411},
   Doi = {10.1287/ijoc.1070.0253}
}
```

To cite this repository use 

```
@Electronic{MOrepo-Pedersen08,
  Title = {Bicriterion assignment and multi modal assignment problems (MOrepo-Pedersen08)},
  Author = {Pedersen, C.R. and Nielsen, L.R.},
  Url = {https://github.com/MCDMSociety/MOrepo-Pedersen08},
  Year = {2008},
  Note = {Instance and result files at MOrepo.}
}
```

To cite the Multi-Objective Optimization Repository use

```
@Electronic{MOrepo,
  Title = {Multi-Objective Optimization Repository (MOrepo)},
  Author = {L. R. Nielsen},
  Url = {https://github.com/MCDMSociety/MOrepo},
  Year = {2017},
}
```

In a paper (written using LaTeX) you may write: 

```
Instances from \cite{Pedersen} are tested which are available from the Multi-Objective 
Optimization Repository (MOrepo) (\cite{MOrepo, MOrepo-Pedersen08}). 
```

Always remember to cite the research paper and not the repository if you don't want to include all
citations.


## Test instances

Instances are named `Template_AP_n<n>.<raw/xml>` where `n` is the size of the problem. The paper considers
instances of size 5-50; however, the instance set also contains 5 instances of size 60-100. Costs
are generated random in [0,30].

All instance files are given in both xml and raw format. The xml format is self explainable (see
e.g. [ex1](./instances/xml/Tuyttens_AP_n05.xml)).


### Raw format description (AP)

We use the following parameter names:

* $n$ = dimension/size
* $c^{k}_{r,c}$ = $k$'th cost of assigning row $r$ to column $c$.

The instances have the following format:

```
n 
c^{0}_{0,0}... c^{0}_{0,n-1}
c^{0}_{1,0}... c^{0}_{1,n-1}
...
c^{0}_{n-1,0}... c^{0}_{n-1,n-1}
c^{1}_{0,0}... c^{1}_{0,n-1}
c^{1}_{1,0}... c^{1}_{1,n-1}
...
c^{1}_{n-1,0}... c^{1}_{n-1,n-1}
```

That is, first the dimension, then the costs for the first criterion and next the cost for the
second criterion.



### Multi modal assignment problems (MMAP)

The instances are contained in the sub folder `MMAP`. Instances are named
`Template_MMAP_d<n>_e<I1>_c<I2>_m<M>_s<S>_<Y>.xml` where `Y` is the instance number of a BiMMAP of
size $n$ with entry range `I1` and cost range `I2` using method `M` and shape `S`.

A total of 8000 instances are provided. That is, 100 instances of each of the
following 80 possible configurations were generated:

- n: 4, 6, 8, 10.
- I1: 2-8 (not for method 2) and 10-30.
- I2: 0-500 and 0-10000.
- (M,S): (1, −60), (1,0), (1, 60), (2, 3), (2, 4), (3, 0).


## Results

Restults are given in the `results` folder using the [json
format](https://github.com/MCDMSociety/MOrepo/blob/master/contribute.md) (see Step 3). 




