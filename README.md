# GitHub Actions DevOps Examples

[![Lint Code Base](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-super-linter.yaml/badge.svg)](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-super-linter.yaml)
[![Docker Build](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-docker-build.yaml/badge.svg)](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-docker-build.yaml)
[![Snyk Scan](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-snyk-scan-image.yaml/badge.svg)](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-snyk-scan-image.yaml)
[![Trivy Scan](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-trivy-scan-image.yaml/badge.svg)](https://github.com/BretFisher/github-actions-templates/actions/workflows/call-trivy-scan-image.yaml)

See this repositories [`.github`](.github) directory for examples on linters, workflows, and dependabot.

## Examples

- [`.github/dependabot.yml`](.github/dependabot.yml) will make PRs for version updates to your workflow steps.
- [`.github/linters/`](.github/linters/) stores linter configs used by Super-Linter.
- [`.github/workflows/call-super-linter.yaml`](.github/workflows/call-super-linter.yaml) is a workflow that calls Super-Linter, which I'm storing the full reusable workflow in [bretfisher/super-linter-workflow](https://github.com/BretFisher/super-linter-workflow).
- [`.github/workflows/call-docker-build.yaml`](.github/workflows/call-docker-build.yaml) is a workflow that calls a Docker build advanced workflow, which I'm storing the full reusable workflow in [bretfisher/docker-build-workflow](bretfisher/docker-build-workflow).
- [`.gitub/workflows/reusable-gitops-pr.yaml]()
- [`.github/workflows/call-docker-build-promotion.yaml']()
- [`.github/workflows/call-snyk-scan-image.yaml`](.github/workflows/call-snyk-scan-image.yaml) is a workflow that calls a [Snyk](https://github.com/snyk/cli) scan image at [`.github/workflows/reusable-snyk-scan-image.yaml`](.github/workflows/reusable-snyk-scan-image.yaml).
- [`.github/workflows/call-trivy-scan-image.yaml`](.github/workflows/call-trivy-scan-image.yaml) is a workflow that calls a [Trivy](https://github.com/marketplace/actions/aqua-security-trivy) scan image at [`.github/workflows/reusable-trivy-scan-image.yaml`](.github/workflows/reusable-trivy-scan-image.yaml).

Some workflows are reusable or are calling other reusable workflows in other repositories.

I name workflows depending on how they are used:

- `reusable-*.yaml` - the workflow is designed to be reusable as a "called" workflow, and have a `workflow_call` event in them. They would exist in a central repository that is either `public` or `internal` and called by other repositories.
- `call-*.yaml` - this calls a reusable workflow that lives in other repositories or files with `uses: <github-path>`.
- Any other workflows are just designed to run inside a repository directly.

## This repository is part of my examples on GitHub Actions

- (you are here) [bretfisher/github-actions-templates](https://github.com/BretFisher/github-actions-templates) - Main reusable templates repository
- [bretfisher/super-linter-workflow](https://github.com/BretFisher/super-linter-workflow) - Reusable linter workflow
- [bretfisher/docker-build-workflow](https://github.com/BretFisher/docker-build-workflow)- Reusable docker build workflow
- [bretfisher/docker-ci-automation](https://github.com/BretFisher/docker-ci-automation) - Step by step video and example of a Docker CI workflow
- [My full list of container examples and tools](https://github.com/bretfisher)

## More reading

- [Docker Build/Push Action advanced examples](https://github.com/docker/build-push-action/tree/master/docs/advanced)
- [My full list of container examples and tools](https://github.com/bretfisher)

## 🎉🎉🎉 Join my container DevOps community 🎉🎉🎉

- [My "Vital DevOps" Discord server](https://devops.fan)
- [My weekly YouTube Live show](https://bret.live)
- [My courses and coupons](https://www.bretfisher.com/courses)
