# Preparing Workflow Package Signing Key

```shell
gpg --quick-generate-key "bgh <arch at bgh dot io>"
gpg --export --armor --output public-key.asc bgh
gpg --export-secret-keys --armor --output private-key.asc bgh
gpg --export-secret-keys --armor bgh | base64 --wrap=0
```
