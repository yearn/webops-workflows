Reuse workflows here for regular devops. For example,

```

name: your repo's pr flow

on:
  pull_request:
    branches: [ main ]

jobs:
  call-reusable-workflow:
    uses: yearn/webops-workflows/.github/workflows/pull-request.yml@main
    with:
      node-version: '20'
      run-tests: true

```
