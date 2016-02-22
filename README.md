# LaTeX

Dockerfile for LaTeX with `blang/latex` as baseimage.

## Usage


### Getting the image

```
docker pull sdelrio/latex 
```

### Build the image

```
docker build -t sdelrio/latex:latest .
```

### Generate pdf from tex document

Output will be written on `build` subdirectoroy.

#### Using pdflatex

```
docker run --rm -v `pwd`:/latex sdelrio/latex make_latex mydocument.tex
```

#### Using xelatex

```
docker run --rm -v `pwd`:/latex sdelrio/latex make_xelatex mydocument.tex
```

### Clean log output

After building pdf if the result has no errors it will delete log, but to force cleanup do

```
docker run --rm -v `pwd`:/latex sdelrio/latex clean
```

