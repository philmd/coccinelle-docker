# coccinelle-docker

Dockerized [Coccinelle](http://coccinelle.lip6.fr) spatch (matching and transformation tool for C).

# Installation

Automated builds of the image are available on [Dockerhub](https://hub.docker.com/r/philmd/coccinelle) and is the recommended method of installation.

Download:

```bash
docker pull philmd/coccinelle:latest
```

Run spatch:

```bash
docker run --rm -v `pwd`:`pwd` -w `pwd` -u `id -u` \
	philmd/coccinelle:latest
			--sp-file myscript.cocci \
			--macro-file mymacro.h \
			--in-place \
			myfile.c
```

Build the image yourself:

```bash
docker build -t philmd/coccinelle github.com/philmd/docker-coccinelle
```
