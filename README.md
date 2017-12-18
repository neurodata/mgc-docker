# MGC Docker Container

## Usage


### Code
Check out the source code for this project at [neurodata/mgc](http://github.com/neurodata/mgc) on Github.

### Documentation

Please check out the `mgc` documentation, available through R with the `help()` function.

### Error Reporting
Experiencing problems? Please read existing [issues](http://github.com/neurodata/mgc/issues) to see if others are experiencing the same problem (don't forget to look at "closed" issues in case it has been fixed), and if you need more assistance open a [new issue](http://github.com/neurodata/ndmg/issues/new) explaining what's happening so we can help.

### Acknowledgement
When using this package, please acknowledge us with the citations from the MGC paper [MGC paper](https://arxiv.org/abs/1609.05148).

### Instructions

The [MGC docker container](https://hub.docker.com/r/neurodata/mgc/) allows users to use the Multiscale Generalized Correlation family of functions for exploring the latent geometric structures captured by the dependent relationships between variables.

Users can set up docker by the following [docker installation](https://docs.docker.com/engine/installation/) tutorial.

The `MGC` docker container can be set up as follows with a properly installed `docker` engine, and will take approximately 1 minute to download on a recommended machine:

```
docker pull neurodata/mgc
docker run -ti --entrypoint /bin/bash <local-path>:<container-path> neurodata/mgc
# <local-path>: the path to data on the host machine.
# <container-path>: the path you want the local folder to appear inside of the running container.
root@5fe9609e040d:/# R

R version 3.4.3 (2017-11-30) -- "Kite-Eating Tree"
Copyright (C) 2017 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

> # a fresh R session
> require(mgc)  # loads the mgc package into the current environment.
```

### Demo

The demo can be run as follows:

```

docker pull neurodata/mgc
docker run -ti --entrypoint /bin/bash <local-path>:<container-path> neurodata/mgc
# <local-path>: the path to data on the host machine.
# <container-path>: the path you want the local folder to appear inside of the running container.
root@5fe9609e040d:/# R

R version 3.4.3 (2017-11-30) -- "Kite-Eating Tree"
Copyright (C) 2017 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

> # a fresh R session
> require(mgc)  # loads the mgc package into the current environment.
> set.seed(12345)
> mgc.sample(mgc::test_xunif, mgc::test_ylin)$statMGC  # test with a linear relationship between x and y
```

and will produce the following result approximately *instantaneously*:

```
0.891153
```

