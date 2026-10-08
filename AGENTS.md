# Isomorphic docs: agent instructions

The public documentation site for Isomorphic, on [Mintlify](https://mintlify.com). Pages are
MDX with YAML frontmatter, configuration is `docs.json`, and every push to `main` deploys. For
Mintlify product knowledge (components, configuration), use the Mintlify docs MCP server at
`https://www.mintlify.com/docs/mcp`.

## Where the truth lives

The product is `isomorphic-team/isomorphic-app`. These pages describe its behavior, so when a
page and the code disagree, the code wins and the page needs fixing. Link to a file in that
repository with a full GitHub URL (`https://github.com/isomorphic-team/isomorphic-app/blob/main/<path>`),
never a relative path, since the file is not in this repo.

## Terminology

- **Brain**: a git repository of markdown that holds a person's or team's knowledge. Not
  "wiki", "vault", or "workspace".
- **Organization** (or **org**): who owns brains and members. Roles are `viewer < editor <
  admin < owner`, and brain roles are separate from org roles.
- **The app**: the viewer and editor, rendered in the conversation as an MCP App or in a browser
  tab. Not "the widget" in prose.
- **OKF**: the Open Knowledge Format, the markdown conventions a brain follows.
- Tool names are code: `write_page`, `view_page`.

## Style

- Plain, specific, second person. Say what happens and why, with the command or file name.
- No em-dashes. Use a comma, a period, parentheses, or a colon.
- Sentence case headings. Code formatting for commands, paths, env vars, and tool names.
- Escape `<` and `{` in prose (`&lt;`, `\{`), or keep them inside backticks; MDX parses them
  as JSX otherwise. Placeholders such as `<your-worker>` belong in code spans.
- Check with `mint broken-links` before pushing.

## Content boundaries

Public, user- and self-hoster-facing material only. Design docs, operator runbooks (`docs/ops/`),
and the roadmap stay in `isomorphic-app`; link to them on GitHub where a page needs them, and do
not copy them here.
