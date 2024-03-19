# DEPRECATED

use a more generic approach like:

```yaml
        uses: giantswarm/install-binary-action@v2
        with:
          binary: "terrarium"
          version: "1.3.2"
          tarball_binary_path: "${binary}"
          download_url: "https://github.com/terrarium-tf/cli/releases/download/v${version}/terrarium_${version}_Linux_amd64.tar.gz"
          smoke_test: "${binary} --version"
```
