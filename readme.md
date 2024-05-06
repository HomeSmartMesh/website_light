# usage

create a workflow in a `workflow.yaml` with this content as example

```yaml
- action: fetcher/fetch
  type: github
  repository: MicroWebStacks/astro-big-doc
  ref: main
  filter: content/*
  resource: test-website
- action: markdown/build
  resource: test-website
  path: /fetch/test-website/content
```

then run

```cmd
docker compose up
```

all actions will run and the build will be available in `./cache` folder

for more details about how this works, see https://github.com/MicroWebStacks/copper
