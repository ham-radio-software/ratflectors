# Public Ratflectors

Known Public Ratflectors for D-Rats use

This is a YAML file that is planned to be used to assist in configuring
the Internet Ratflector lists for D-Rats.

This file is maintained in [YAML](https://yaml.org/spec/) format

Each entry has the following members:

* Name, a short name, about 8 characters may be normally visible.
* Description, More detailed description.
* Hostname, Fully qualified host name.
* Port, port number.
* Active, true for active at last update.

An optional password member is if a password is needed.  The password
should not be stored in this file.

Advanced maintainers can copy the tests/pre-commit script to .git/hooks which
if the proper tools are installed, will test the format of the files in a
git commit action.  This requires shellcheck, yamllint, and codespell to be
installed.

```yaml
---
ratflectors:
  - name: short_name
    description: |
      Long description of the Ratflector that can take
      multiple lines, including contact information if known.
    hostname: ratflector.example.com
    port: 9000
    active: true
    password: false
```
