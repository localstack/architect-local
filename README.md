# Architect Local

This repo provides `arclocal`, a simple command-line wrapper to use Architect CLI (https://arc.codes) locally with [LocalStack](https://localstack.cloud).

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

... should print something like:
```
App ⌁ sample
Region ⌁ us-west-2
Profile ⌁ default
Version ⌁ Architect 9.0.0

⚬ Deploy Creating new private deployment bucket: sample-cfn-deployments-e4e7d
⚬ Deploy Initializing deployment
| Stack ... SampleStaging
| Bucket .. sample-cfn-deployments-e4e7d
✓ Hydrate Finished checks, nothing to hydrate
⚬ Deploy Created deployment templates
✓ Deploy Generated CloudFormation deployment
✓ Deploy Deployed & built infrastructure
✓ Success! Deployed app in 37.008 seconds

http://95da73ea.execute-api.localhost.localstack.cloud:4566
```

You can then access http://95da73ea.execute-api.localhost.localstack.cloud:4566 in your browser to see the Architect demo landing page, deployed in your LocalStack instance.

(Please note that LocalStack needs to be running and listening on the default port 4566 for the above commands to succeed.)

## Change Log

* v0.0.3: Fix patching, print local endpoints after deployment, update README
* v0.0.1: Initial version

## License

This tool is provided under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).
