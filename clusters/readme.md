# Root Cluster Name Directory

## Overview

This directory is the root of configured cluster. Each file in this directory is loaded for the appropriate context.

### apps.yaml

- This file contains a link to the appropriate configuration of apps on the root of the project.

### install-*.yaml

- We put install-* files here so we can set install dependencies on the rest of the stacks. This is necessary to address CRDs and make sure that they are installed before we apply configurations.

### kustomized-infra.yaml

- This file points to the '/infrastructure/kustomized' directory. This is where we declare configurations that vary by environment. We manage the differences by pointing to overlays.

### namespaces.yaml

- This file holds namespaces that are required for the various packages and configurations that we run.

### Sources

- Sources are helm source definitions that point to helm repos.

### static-infra.yaml

- This file points to the 'static-infra' directory. This is where we declare configurations that do not vary by environment. These have no overlays.
