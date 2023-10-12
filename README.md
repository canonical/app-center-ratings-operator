# Ubuntu Ratings Service Operator

This is an operator that enables the Ubuntu Software Centre backend ratings service to run on
Kubernetes with Juju, integrating with PostgreSQL for its database.

## Getting Started

First ensure that you have an appropriate [development setup](https://juju.is/docs/sdk/dev-setup) for Juju.

```shell
charmcraft pack

juju add-model ratings

juju deploy ./ubuntu-software-ratings_ubuntu-22.04-amd64.charm ratings

juju deploy postgresql --channel edge 

juju relate ratings postgresql
```
