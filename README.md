# HashiCorp envconsul Action

## Usage

Here's an example of how to use this action in a workflow file:

```yaml
name: Example Workflow

on:
  workflow_dispatch:

jobs:
  say-hello:
    name: Say Hello
    runs-on: ubuntu-latest

    steps:
      - name: Fetch secrets
        uses: mdminhazulhaque/hashicorp-envconsul-action@main
        with:
          vault-addr: https://vault.example.com
          vault-token: hvs.1234567890
          vault-secret: kv/prod-api
          env-file: .env
```
