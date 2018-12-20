# Gradle plugin for 'pre-commit'

This repo is a shim that adds [gradle](https://gradle.org/) support to [pre-commit](https://pre-commit.com).

## Installing

### Pre Commit 

Install pre-commit according to the website (https://pre-commit.com/#install).


### Enable Pre-Commit

Create `.pre-commit-config.yaml` in your project root with the following content:

```yaml filename=.pre-commit-config.yaml
# .pre-commit-config.yaml
exclude: '^$'
fail_fast: false
repos:
-   repo: https://github.com/neuhalje/pre-commit-gradle.git
    rev: master
    hooks:
    -   id: gradle-check
```

Now enable pre-commit via `pre-commit install`.
