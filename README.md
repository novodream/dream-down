# dream-up

Destroy resources with DReAM CLI down command

## Usage

```yaml
    - name: Undeploy
      uses: @novodream/dream-down@main
      with:
        workspace: staging
        private-key: ${{ secrets.PRIVATE_KEY }}
```

This action is typically used in conjunction with [novodream/setup-dream](https://github.com/novodream/setup-dream)
action.

```yaml

steps:
  - uses: actions/checkout@v3
    with:
      fetch-depth: 0 # not mandatory but required by certain DReAM packages

  - name: Setup DReAM CLI
    uses: novodream/setup-dream@main
    with:
      token: ${{ secrets.DREAM_TOKEN }}

  - name: Undeploy
    uses: @novodream/dream-down@main
    with:
      workspace: staging
      private-key: ${{ secrets.PRIVATE_KEY }}
```
