# Publish VSCode Extension

Action used for deploying a static website to [Surge](https://surge.sh/).

## Usage

```yaml
on:
  push:
    branches: [master]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Deploy to Surge
        uses: mrzli-gh-actions/deploy-to-surge@v1.0.0
        with:
          root-dir: ./public
          surge-domain: ${{ secrets.SURGE_DOMAIN }}
          surge-token: ${{ secrets.SURGE_TOKEN }}
```