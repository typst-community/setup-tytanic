# Setup Tytanic
This action provides the [Tytanic] CLI to subsequent steps in GitHub Actions.

```yaml
- uses: typst-community/setup-tytanic@v1
- run: tt run
```

## Usage
### Basic usage
```yaml
name: Build GitHub-Pages
on: push
jobs:
  build-docs:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: typst-community/setup-tytanic@v1
        with:
          tytanic-version: 0.3.0
      - run: tt run
```

### Inputs & Outputs
See [action.yml](action.yml) for a the inputs and outputs of this action.

## Contributions
A contribution guide can be found [here](docs/CONTRIBUTING.md). You can view the changelog of previous contributions and release [here](docs/CHANGELOG.md).

## Credit
This action is in large part inspired by [setup-typst].

[setup-typst]: https://github.com/typst-community/setup-typst
[Tytanic]: https://github.com/typst-community/tytanic
