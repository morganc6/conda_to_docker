# conda_to_docker
how to convert conda environment into docker

The following example details how to convert a conda environment that is set up to run gatk4 with all dependecies into a docker image.

conda activate gatk4

conda env export > gatk4.yml

conda activate coiled # installed coiled as its own environment

python create_docker.py

singularity pull gatk4.sif docker://morganc6/morganc6-gatk4
