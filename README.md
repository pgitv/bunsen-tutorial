# Bunsen Tutorial
This repository contains a tutorial for exploring FHIR data with Apache Spark in an interactive notebook. This is supported with the [Bunsen library](http://engineering.cerner.com/bunsen), and uses synthetic data generated by the [Synthea project](https://synthetichealth.github.io/synthea/) to eliminate data security concerns.

## Prerequisites
The easiest way to run this is in a Docker container. If you don't have Docker already, download and install the [community edition here](https://www.docker.com/get-docker).

Next, the Bunsen project offers a Docker container that includes it, [Project Jupyter](http://jupyter.org/), [Apache Spark](https://spark.apache.org/), and needed dependencies. This totals about 5 gigabytes when uncompressed, but that includes common OS and Python images that may be used for other needs. All of it is installed with the following command:

```bash
docker pull cerner/bunsen-notebook
```

See the [Bunsen Docker documentation](http://engineering.cerner.com/bunsen/0.4.0/docker.html) for more information.

## Launch the Tutorial
Once the above Docker image is installed, clone or download this bunsen-tutorial git repository. Then change your directory to the bunsen-tutorial folder and launch the tutorial with the following command:

```bash
docker run -p 8888:8888 -p 4040:4040 -v $PWD:/home/jovyan/work cerner/bunsen-notebook
```
or on Windows:

```bash
docker run -p 8888:8888 -p 4040:4040 -v %cd%:/home/jovyan/work cerner/bunsen-notebook
```

Click on the URL displayed at the bottom of the screen and Jupyter will open in your web browser. From there, navigate to work/getting_started.ipynb. From there, just follow the instructions in that notebook!

First-time users can simply read the instructions and execute the cells. As you become familiar with the system, feel free to experiment by editing queries or code and seeing what happens. Any changes you make will be saved to your copy of the notebooks themselves.
