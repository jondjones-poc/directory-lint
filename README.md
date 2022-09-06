# Example of how to use ls-lint - By Jon D Jones 💥

Example of how to use [ls-lint](https://github.com/loeffel-io/ls-lint).  

## Live Demo 👻

 [https://opti-fullstack-sdk.jonjones.workers.dev/](https://opti-fullstack-sdk.jonjones.workers.dev/)

## Steps To Get Started

To install the package:

```
npm install @ls-lint/ls-lint
```

Next, add this to your scripts:

```
"lint": "node_modules/.bin/ls-lint"
```

Create file `.ls-lint.yml`

```
# .ls-lint.yml

ls:
  .dir: regex:[a-z0-9\-]+
  .js: kebab-case
  .css: kebab-case
  .html: kebab-case
  .json: kebab-case
  .ts: kebab-case

  dist:
    .js: point.case

  benchmarks/ssr:
    .js: camelCase

ignore:
  - node_modules
  - .git
```

Run script

```
npm run lint
```


