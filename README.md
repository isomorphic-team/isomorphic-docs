# Isomorphic docs

The public documentation for [Isomorphic](https://isomorphic.sh), built with
[Mintlify](https://mintlify.com). The product's code lives in
[isomorphic-team/isomorphic-app](https://github.com/isomorphic-team/isomorphic-app).

## Run it locally

```sh
npm i -g mint
mint dev            # http://localhost:3000
```

The Mintlify CLI refuses Node 25 and newer. On a machine without an LTS Node, run it through a
temporary Node 22:

```sh
npx -y node@22 "$(readlink -f "$(which mint)")" dev
```

`mint broken-links` checks every internal link. Run it before pushing.

## Publishing

The Mintlify GitHub app deploys every push to `main`. A merge is a release.

## Layout

| File                   | Holds                                                   |
| ---------------------- | ------------------------------------------------------- |
| `docs.json`            | Navigation, branding, navbar, footer                    |
| `*.mdx`                | One page each; `title` and `description` in frontmatter |
| `images/`              | Screenshots, referenced as `/images/<name>.png`         |
| `logo/`, `favicon.svg` | The mark, matching `isomorphic.sh`                      |
