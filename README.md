# GitHub Action: preparing a Debian-like container

Preparing a Debian-like image for doing stuff like Python tests or linting

It performs the following things:
* Updating all packages
* Installing locales and gettext
* Updating locales

## Example

```yaml
    steps:
      - uses: actions/checkout@v4
      - uses: fbrehm/prepare-debian-container@v1
```

## Inputs

```yaml
inputs:
  manage_locales:
    description: PyPI username
    required: false
    default: true
```



