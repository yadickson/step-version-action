STEP VERSION ACTION
===================

Step to get and share version.txt file only with version number


* Use

```yaml
on: [push]

jobs:
  test_step_version_action:
    runs-on: ubuntu-latest
    name: getting version
    steps:
      - name: checkout code
        uses: actions/checkout@v5
      - id: version
        uses: yadickson/step-version-action@v1
      - run: echo "project version ${PROJECT_VERSION}"
        shell: bash
        env:
          PROJECT_VERSION: ${{ steps.version.outputs.version }}

```
