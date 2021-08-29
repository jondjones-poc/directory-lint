#

https://github.com/loeffel-io/ls-lint

install

```
npm install @ls-lint/ls-lint
```

Add script

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