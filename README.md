# charts

## Steps for adding new helm chart

Once you have a helm chart ready, follow the steps to add it in the chart repo

- Validate helm chart

  ```bash
  $ helm lint example/alpine/
  ```
  Fix helm lint issues if there are any.

- Package the helm chart

  ```bash
  $ helm package examples/alpine
  ```

- Create a branch on top of `gh-pages`

- Add helm chart package to `arriqaaq/charts`

- Build the index

  ```bash
  $ helm repo index --url https://arriqaaq.github.io/charts --merge index.yaml .
  ```

- Commit, push and raise a PR against `gh-pages`
