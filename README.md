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

## Branch Management

The `master` branch is write-protected, and cannot be
directly pushed to.

To make changes to the `master` branch, approved pull
requests have to be merged into it. This encourages the
creation of features branches, which helps to avoid merge
conflicts.

To create a feature branch, create a new branch from master:

```bash
# On master branch
$ git branch -b <USERNAME>/<MY-FEATURE-NAME>
```



### Merging a Feature Branch

When you are finished working on a feature branch, open a
PR, and ask someone to review and approve it. Then, rebase
the branch on master:

```bash
# On feature branch
$ git rebase master
```

Optionally, squash some commits:

```bash
# On feature branch
$ git rebase master -i
```

Then, force push, switch to master, merge and push to
master.
```bash
# On feature branch
$ git push --force
$ git checkout master
$ git merge <USERNAME>/<MY-FEATURE-NAME>
$ git push
```


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
