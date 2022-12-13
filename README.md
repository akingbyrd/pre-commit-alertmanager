# pre-commit-alertmanager

Pre commit checks for valid syntax of [alert manager](https://prometheus.io/docs/alerting/latest/overview/) config and rule files

Taken from the original prometheus pre-commit [hook](https://github.com/fortman/pre-commit-prometheus) 

This is a plugin for [pre-commit](https://pre-commit.com)

### Usage

To lint Alert Manager Config files, use the `alertmanager-config` hook. 

    - repo: https://github.com/akingbyrd/pre-commit-alertmanager
      rev: v0.0.1
      hooks:
      - id: check-config
        entry: --entrypoint /bin/aktool prom/alertmanager:latest
        files: >
          (?x)^(
            config_directory/.*\.yml
          )$

