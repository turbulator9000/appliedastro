# how to write a new post

## 1. make a file in `_posts/`

the name has to be `YYYY-MM-DD-some-title.md`, e.g. `_posts/2026-10-20-mit-bee-practice.md`.

## 2. start it with this header

```markdown
---
title: mit bee practice round
tags: [integration bee]
---

your post starts here.
```

tags so far: `integration bee`, `notes site`, `astro`, `math`, `meta` — make up new ones whenever.

## 3. write in markdown, math in `$$`

| you type | you get |
|---|---|
| `the answer is $$\frac{\pi}{4}$$ nice` | inline math inside the sentence |
| `$$` on its own line, equation, `$$` on its own line | big centered equation |

notes:
- use `$$` for inline math too (not single `$`) — markdown can mangle single-dollar math
- `\begin{aligned} ... \end{aligned}` works for multi-line steps; put it inside a `$$` block
- if a literal `|` in math breaks a table, write `\vert` instead
- never write two braces back to back like `{{` or `}}` — the site builder reads those as its own commands. add a space: `\frac{ {a} }{b}`

## 4. publish

**easiest (no terminal):** on github.com open the repo → `_posts` → **add file → create new file**, paste the post, click **commit**. the site updates in ~1 minute.

**from your mac:** save the file, then
```
git add . && git commit -m "new post" && git push
```

## images

drop them in `assets/` and write `![what it shows]({{ site.baseurl }}/assets/name.png)`.
