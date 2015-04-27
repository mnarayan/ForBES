# ForBES

**ForBES** (standing for **For**ward-**B**ackward **E**nvelope **S**olver) is a MATLAB solver for
nonsmooth convex optimization problems.

It is generic in the sense that the user can customize the problem to solve in an easy and flexible way.
It is efficient since it features very efficient algorithms, suited for large scale applications.

For exhaustive documentation on how to use ForBES, please refer to [ForBES webpage](http://lostella.github.io/ForBES/).

## Installation

Simply clone the git repository, or click on this [link](https://github.com/lostella/ForBES/archive/master.zip)
to download it as a zip archive and decompress the archive. Then move with the MATLAB command line to
the directory of ForBES. Compile all the *mex*-files required by simply hitting

```
> make
```

## How to use it

ForBES consists mainly of two MATLAB routines, `minfbe` and `miname`.
In order to use them one must provide a description of the problem in a MATLAB
structure and (optionally) a set of options:

```
out = minfbe(prob, opt);
out = miname(prob, opt);
```

Structure `prob` contains attributes describing the details of the problem, such as objective
terms and constraints, while `opt` describes, e.g., details on the algorithm to use, termination
criteria, the level of verbosity, and so on. Output `out` will contain the results of the optimization process.
Details on how to specify these structures can be found [here](http://lostella.github.io/ForBES/).

Examples on how to use `minfbe` and `miname` can be found in the [tests folder](https://github.com/lostella/ForBES/tree/master/tests). Furthermore, you can access the help file of the solvers directly from MATLAB with

```
> help minfbe
> help miname
```

## Credits

ForBES is developed by Lorenzo Stella [`lorenzo.stella-at-imtlucca.it`] and Panos Patrinos [`panagiotis.patrinos-at-imtlucca.it`]. Any feedback, bug report or suggestion for future improvements is more than welcome. We recommend using the [issue tracker](https://github.com/lostella/ForBES/issues) to report bugs.