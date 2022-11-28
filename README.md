# Self hosted runner workspace cleaner
Clean left over files from previous builds. Also cleans the runners SSH config.

### Usage
Run this action before running `actions/setup` to clean all of the files form the previous run. 
```yaml
jobs:
  your_job:
    name: Your job
    runs-on: self-hosted
    steps:
      - uses: Vendic/github-self-hosted-runner-workspace-cleaner@master

      - uses: actions/checkout@v3

      - name: Do your stuff
        run: echo "Hello world"
```
