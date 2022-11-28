# Ansible-vault-pre-commit

A [pre-commit](http://pre-commit.com) hook that check for ansible-vault
encryption

## Hooks

### encryption-check
Verifies that vault files are encrypted. Defaults to checking files starting
with `vault`, ending with `.vault.yml` or ending in `.vault`

```yaml
# usage
repos:
  - repo: https://github.com/pypeaday/ansible-vault-pre-commit
    rev: v1.0
    hooks:
      - id: encryption-check
        name: Ansible Vault Encryption Check
        description: Checks that task files are encrypted
        entry: encryption-check.sh
        # override files to all files in ./tasks/ directory
        files: ((^|/)tasks)
        language: script

```

# Credit

[iamthefij](https://git.iamthefij.com/iamthefij/ansible-pre-commit/src/branch/master)
