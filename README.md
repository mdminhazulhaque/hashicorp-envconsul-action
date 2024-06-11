# HashiCorp envconsul Action

Fetch HashiCorp Vault Secrets as a `.env` file using the official `envconsul` tool.

## Usage

Here's an example of how to use this action in a workflow file:

```yaml
name: Fetch Secrets
on:
  workflow_dispatch:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Fetch secrets
        uses: mdminhazulhaque/hashicorp-envconsul-action@main
        with:
          vault-addr: https://vault.example.com # must use http or https
          vault-token: hvs.E589279A38BE         # generate fine tuned token
          vault-secret: kv/prod-api             # secret path, kv or kv2
          env-file: .env                        # file name to be created
```
