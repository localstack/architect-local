# Architect Local

This repo provides `arclocal`, a simple command-line wrapper to use Architect CLI (arc.codes) locally with [LocalStack](https://localstack.cloud).

## Prerequisites

* [LocalStack](https://github.com/localstack/localstack)
* [`awslocal`](https://github.com/localstack/awscli-local)
* `npm`

## Installing

The `arclocal` CLI can be installed via `npm`:
```
npm install -g architect-local @architect/architect
```

Please note that the command above includes the `@architect/architect` package - the `arclocal` allows to install arbitrary versions of `@architect/architect` under the covers.

## Usage

The `arclocal` CLI has the same usage as the `arc` command. For example, to initialize and deploy an app locally to your LocalStack instance:
```
arclocal init
arclocal deploy
```

(Please note that LocalStack needs to be running and listening on the default port 4566 for the above commands to succeed.)

## Change Log

* v0.0.3: Fix patching, print local endpoints after deployment, update README
* v0.0.1: Initial version

## License

This tool is provided under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).
