<h1>
<p align="center">
  ⚙️
  <br>actions
</h1>
  <p align="center">
    An assortment of GitHub actions I use in my personal projects.
  </p>
</p>

## Usage

There are two types of action definitions in this repo. Reusable workflows, and composite actions.

For more info on reusable workflows, check out the [reusable workflow documentation](https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows) from github.

For more info on composite actions, check out the [composite action documentation](https://docs.github.com/en/actions/tutorials/create-actions/create-a-composite-action) from github.

### Reusable workflows

Reusable workflows are called with the `uses` keyword directly inside a job. There's no need to specify a step. See [jobs.<job_id>.uses](https://docs.github.com/en/actions/reference/workflows-and-actions/workflow-syntax#jobsjob_iduses) Here's an example of re-using the bevy-ci workflow.

```yaml
name: ⚙️ CI

on:
  - pull_request

jobs:
  ci:
    name: 🕊️ Bevy CI
    uses: jkaloger/actions/.github/workflows/bevy-ci.yml@{SHA}
```

I recommend pinning to a specific SHA for stability.

### Composite Actions

(todo)
