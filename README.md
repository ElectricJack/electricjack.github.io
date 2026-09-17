# electricjack.github.io

Publishes the villa website at **https://electricjack.github.io/**.

The website source, assets and tests remain in [ElectricJack/jackkern.com](https://github.com/ElectricJack/jackkern.com). This repository owns the root GitHub Pages deployment. Its workflow checks out the selected source revision, builds the site and all static fallback images, checks local links, then publishes `dist/`.

To publish the latest source:

```sh
gh workflow run deploy.yml --repo ElectricJack/electricjack.github.io -f source_ref=main
```

For a specific tested revision, replace `main` with its commit SHA. The deployed `deployment.json` records both the website source revision and this repository's deployment revision.

Pages uses **GitHub Actions**, with no custom domain. `index.md` and `_config.yml` retain the former 2019 placeholder source; they are not published by the workflow.
