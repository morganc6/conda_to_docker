# how to convert conda environment into docker


The following example details how to convert a conda environment that is set up to run gatk4 with all dependecies into a docker image.

The basis of this follows the instructions provided in the [Using Coiled as a Docker Image pipeline](https://towardsdatascience.com/converting-conda-pip-environments-into-docker-images-d02aa22e872c)


1. activate gatk4 conda environment
```
conda activate gatk4
```

2. export environment to .yml file
```
conda env export > gatk4.yml
```

3. activate coiled environment
```
conda activate coiled 
```

4. create docker file from gatk4.yml file.

```
python create_docker.py
```

5. download the gatk4 docker image from docker
```
singularity pull gatk4.sif docker://morganc6/morganc6-gatk4
```
