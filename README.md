# OpenWeather Collection

This repository contains the OpenWeather collection of tests and fixtures.

Getting started

- Initialize a local git repository (if not already):

```bash
git init
git branch -M main
git add .
git commit -m "Initial commit: add Azure pipeline and docs"
```

- Create a GitHub repository and push:

```bash
git remote add origin <your-github-repo-url>
git push -u origin main
```

CI with Azure Pipelines

This repository includes `azure-pipelines.yml` which lints YAML files with `yamllint`.
To enable CI:

1. In Azure DevOps create a new pipeline and point it to this repository.
2. Use the existing `azure-pipelines.yml` at the repository root.

# bruno
