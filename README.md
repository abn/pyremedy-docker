# PyRemedy Docker
Docker packaging for [PyRemedy](http://pyremedy.readthedocs.io/en/latest/) library. This is intended as a template for your custom environment builds. By default the container includes 9.10 version of the linux API package from [RRR](https://rrr.se/cgi/index?pg=arapi).

### Usage
In order to run a PyRemedy script, you can mount it in to the container and execute as shown below. In this example we assume `example.py` script to be in the `scripts` directory.
```sh
docker run --rm -it -v `pwd`/scripts:/scripts alectolytic/pyremedy example.py
```

### Build Image
```sh
docker build \
  --build-arg ARG PYREMEDY_VERSION=0.2.1 \
  --build-arg ARG ARAPI_VERSION=910 \
  --tag local/pyremedy .
```
