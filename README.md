# Meru Temporal

The workflow engine of **Meru**, a small in-house container platform (CaaS) on k3s: [Temporal](https://temporal.io)
runs Meru's long-running jobs (a request's approvals, the PRs it opens, waiting for them to merge). Argo CD deploys it
from [Meru/meru](https://git.clockmost.com/Meru/meru) `platform/temporal.yaml` (the upstream Helm chart) and its
database from this repo (`platform/temporal-db.yaml`).

- `database/cluster.yaml` - Temporal's Postgres: one CloudNativePG cluster with two databases (`temporal`,
  `temporal_visibility`). Its passwords are made by CNPG and never in this repo.

## License

MIT - see `LICENSE`.
