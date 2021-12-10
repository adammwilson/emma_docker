# EMMA Docker Container


# Instructions


## Quickstart
```
docker run --rm -p 8787:8787 -e PASSWORD=yourpasswordhere adamwilsonlab/emma:latest
```

Visit `localhost:8787` in your browser and log in with username rstudio and the password you set. NB: Setting a password is now REQUIRED. Container will error otherwise.


## Local machine (no password)

If you are running on a local machine with other security mechanisms, you can use the following:

```
docker run --rm \
  -p 127.0.0.1:8787:8787 \
  -e DISABLE_AUTH=true \
  adamwilsonlab/emma:latest
```

## Singularity

```
cd /panasas/scratch/grp-adamw/singularity/adamw
wget https://github.com/AdamWilsonLab/emma_docker/releases/download/0.0.520/AdamWilsonLab-emma_docker.latest.sif.zip
unzip AdamWilsonLab-emma_docker.latest.sif.zip
singularity pull docker://adamwilsonlab/emma:latest
```
