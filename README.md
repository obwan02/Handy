# Handy

Handy is an app that reads sign language gestures.

## Setup

This app uses conda to manage dependencies. As such, you
will need to create a new envrionment. To do this, run the
follwing code snippet:

```bash
conda env create -n <ENV_NAME> --file environment.yml
```

Note that this code snippet only has to be run once. See the
[sharing environmens section](#Sharing-Environments) for
instructions on how to keep your environment up-to-date.

## Sharing Environments

When sharing a conda environment, the environment might
change over time. To keep up-to-date with the environment
(defined by the `environment.yml` file, run the following
command whenever the environment is changed:

```bash
conda env update --file environment.yml  --prune
```

[See the conda reference for more details on sharing
environments](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment)
