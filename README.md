# lab-tpl-do-pipeline-reusable-workflows

Workflows reutilizables de GitHub Actions del laboratorio.

| Workflow | Qué hace |
|---|---|
| `docker-ci.yml` | Rama → ambiente → tag (`av`/`bv`/`v`), build, push a ECR y tag Git |
| `approval.yml` | Espera la aprobación del environment de GitHub |
| `sync-tag.yml` | Escribe el tag en `<app>/<env>/app.yaml` del repo GitOps |

Los consumidores lo usan fijando un tag: `uses: <dueño>/lab-tpl-do-pipeline-reusable-workflows/.github/workflows/docker-ci.yml@v1.0.0`.
