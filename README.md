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
        with:
          additional_locales: de_DE.UTF-8 fr_FR.UTF-8
```

## Inputs

```yaml
inputs:
  manage_locales:
    description: Should locales be installed and updated on this image
    required: false
    default: true
  additional_locales:
    description: A whitespace separated list of additional locales (except en_US.UTF-8)
    required: false
    default: 'de_DE.UTF-8'
```



