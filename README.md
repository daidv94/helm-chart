# My Helm chart

- We use ghcr.io (or any OCI-compatible container registry will do). Helm has supported this since v3.7(8?) IIRC.

- We use GitHub Actions for linting, testing and release.
    - Linting and testing is done with [chart-testing](https://github.com/helm/chart-testing) and [kind](https://kind.sigs.k8s.io).
    - You can run `./hack/lint.sh` to perform linting on your local machine without actually pushing to the repo.
    - [helm-docs](https://github.com/norwoodj/helm-docs) is used for generating up-to-date chart's README. We also check whether docs are up-to-date in CI. Make sure to run `./hack/gen-docs.sh` once you've done making the changes to the chart.
    - Releases are done automatically when merge to main.


## Usage

```shell
# login to registry and then
helm pull oci://ghcr.io/galaxyfinx/product-helm-charts/app --version 1.0.8
```

## TODO

- [ ] Use S3 for hosting chart along with OCI maybe? Since Harness.io doesn't support OCI registry for Helm yet.
- [ ] Use Harness.io instead of GitHub Actions.

## License

[LICENSE](./LICENSE)
