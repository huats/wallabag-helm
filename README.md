# Helm Chart for Wallabag

This repository, including the issues, focus on deploying wallabag chart via helm.  So for the functionality issues or questions of Wallabag, please open issues on [wallabag/wallabag](https://github.com/wallabag/wallabag)

## Introduction

This [Helm](https://github.com/kubernetes/helm) chart installs [wallabag](https://github.com/wallabag/wallabag) in a Kubernetes cluster. Welcome to [contribute](CONTRIBUTING.md) to Helm Chart for wallabag.

## Prerequisites

- Kubernetes cluster 1.12+
- Helm 3.0+

## Installation

### Add Helm repository

```bash
helm repo add wallabag https://huats.github.io
```

### Configure the chart

The chart can be configured using the traditonal values usage of Helm.
Meanwhile to help a faster deployment, some example of deployments are provided :

- sqlite. You can choose to use a PVC or not for persistence
- MariaDB (including the deployment of the MariaDB container using Bitnami's
  Helm Chart)
- Postrgres (including the deployment of the Postgres container using Bitnami's
  Helm Chart)


### Install the chart

Install the Wallabag helm chart with a release name `my-release`:

```bash
helm install my-release huats/wallabag
```

If you want to use some values on your own, use -f and the path to your
values.yaml file.

```bash
 helm install my-release huats/wallabag -f my-values.yaml
 ``` 

## Uninstallation

To uninstall/delete the `my-release` deployment:

```bash
helm uninstall my-release
```

