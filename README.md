# Vertex plugin template

A [Vertex](https://github.com/CTRL-Neo-Studios/vertex) plugin to start from: a panel view with a string in the
window's language, an asset and one of the app's buttons, built with
[`@type32/vertex-plugin`](https://www.npmjs.com/package/@type32/vertex-plugin).

## Make it yours

1. **Use this template** on GitHub, then clone your repository.
2. Pick an id (lowercase, `-` between words) and put it in place of `my-plugin` in `plugin.json`, `package.json`,
   `locales/*.json` (the key under `plugins`) and `src/` (the view's id and its strings' keys).
3. Fill in `plugin.json`'s `name`, `description`, `author` and `repository`.

## Develop

```sh
bun install
bun run build       # dist/, the folder Vertex installs, and plugin.zip
bun run typecheck
```

In Vertex: Settings → Plugins → Install… ▾ → **From a folder (development)…**, and pick this folder (Vertex finds the
build in `dist/`). Vertex watches it: run `bunx vite build --watch` and the window reloads with each build.

## Release

Push a tag with `plugin.json`'s version (`git tag v0.1.0 && git push --tags`). The workflow in
`.github/workflows/release.yml` builds the plugin and makes a release with `plugin.zip`; Vertex installs from the
repository's latest release and finds updates there.

## Docs

The author docs ship with the SDK, in `node_modules/@type32/vertex-plugin/docs/`, and are on GitHub in
[`packages/vertex-plugin/docs`](https://github.com/CTRL-Neo-Studios/vertex/tree/dev/packages/vertex-plugin/docs).
