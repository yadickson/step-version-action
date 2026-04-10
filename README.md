Actions
=======

**actions/version**

Step to get and share version.txt file only with version number


*How to use*

```yaml
on: [push]

jobs:
  test_step_version_action:
    runs-on: ubuntu-latest
    name: getting version
    steps:
      - id: version
        uses: yadickson/version@REF
        with:
          gist-id: ${{ secrets.GIST_ID }}
          gist-token: ${{ secrets.GIST_TOKEN }}
```

**actions/install**

Step to install dependencies


*How to use*

```yaml
on: [push]

jobs:
  test_step_install_action:
    runs-on: ubuntu-latest
    name: installing project
    steps:
      - uses: yadickson/install@REF
```

**actions/build**

Step to build project


*How to use*

```yaml
on: [push]

jobs:
  test_step_build_action:
    runs-on: ubuntu-latest
    name: building project
    steps:
      - uses: yadickson/build@REF
```

**actions/lint**

Step to check static code project


*How to use*

```yaml
on: [push]

jobs:
  test_step_lint_action:
    runs-on: ubuntu-latest
    name: checking static code project
    steps:
      - uses: yadickson/lint@REF
```

**actions/test**

Step to run unit test


*How to use*

```yaml
on: [push]

jobs:
  test_step_test_action:
    runs-on: ubuntu-latest
    name: running unit test
    steps:
      - uses: yadickson/test@REF
        with:
          gist-id: ${{ secrets.GIST_ID }}
          gist-token: ${{ secrets.GIST_TOKEN }}
```

**actions/coverage**

Step to create coverage report


*How to use*

```yaml
on: [push]

jobs:
  test_step_coverage_action:
    runs-on: ubuntu-latest
    name: creating coverage report
    steps:
      - uses: yadickson/coverage@REF
        with:
          gist-id: ${{ secrets.GIST_ID }}
          gist-token: ${{ secrets.GIST_TOKEN }}
```

**actions/mutation**

Step to run mutation test


*How to use*

```yaml
on: [push]

jobs:
  test_step_mutation_action:
    runs-on: ubuntu-latest
    name: running mutation test
    steps:
      - uses: yadickson/mutation@REF
        with:
          gist-id: ${{ secrets.GIST_ID }}
          gist-token: ${{ secrets.GIST_TOKEN }}
```

**actions/badge**

Step to create badge files into gist


*How to use*

```yaml
on: [push]

jobs:
  test_step_badge_action:
    runs-on: ubuntu-latest
    name: creating badge files
    steps:
      - uses: yadickson/badge@REF
        with:
          gist-id: ${{ secrets.GIST_ID }}
          gist-token: ${{ secrets.GIST_TOKEN }}
```
