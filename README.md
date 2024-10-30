![Maintainer](https://img.shields.io/badge/Maintained%20By-Anvaya%20Cloud-brightgreen) [![ActionLint GitHub Action Workflow](https://github.com/anvayacloud/action-linting/actions/workflows/main.yaml/badge.svg)](https://github.com/anvayacloud/action-linting/actions/workflows/main.yaml) 

# Introduction

This GitHub action is used to perform the linting of GitHub Action templates.

## Example

```yaml
name: GitHub Workflow
on:
  push:
    branches:
      - main
jobs:
  action-lint:
    name: Action Linting
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2

    - name: Run Action Linting
      uses: anvayacloud/action-linting@main
```

## Action Linting Options

Additionally you can pass supported actionlint option or flags with the `arguments` input parameter.

For Example:

```yaml
    ...
    - name: Run Action Linting
      uses: anvayacloud/action-linting@v0.0.1
      with:
        arguments: "-color"
```

## Action Linting Skip Rules

Additionally you can skip rules with -ignore argument. 

For Example:
```yaml
    ...
    - name: Run Action Linting
      uses: anvayacloud/action-linting@v0.0.1
      with:
        files: main.yaml
        arguments: "-color -ignore 'SC2016:'"
```

## Contributing
We would love you to contribute to `@anvayacloud/action-linting`, pull requests are welcome! Please see the [CONTRIBUTING.md](CONTRIBUTING.md) for more information.

## License
The scripts and documentation in this project are released under the [MIT License](LICENSE)
