# jargons.dev Content

This repository contains the content published by [jargons.dev](https://jargons.dev), a community-maintained dictionary of software engineering and technology terms.

The content is kept separate from the website application so contributors can propose content changes without changing application code. The site is being connected to this repository through Astro's content layer.

## Content Structure

Content is grouped by type:

```text
dictionary/  Dictionary entries in MDX (available now)
```

Each category has its own format and validation rules. The dictionary format below is currently in use. Article and clip formats will be documented here when those collections are introduced.

## Dictionary Entries

Create one `.mdx` file per term in `dictionary/`. Use a lowercase, hyphen-separated filename that matches the term's URL slug, such as `access-modifiers.mdx`.

Each entry must have a `title` in its frontmatter. Put the definition and examples in the MDX body:

```mdx
---
title: "Example Term"
---

Explain the term in clear, direct language. Add examples where they help readers understand it.
```

Keep entries focused and accessible. Use headings and lists to organize longer explanations, and fenced code blocks with a language identifier for code examples. Do not add Astro layout paths, page URLs, or other application-specific presentation settings; the website controls how content is rendered.

## Contributing

1. Fork this repository and create a branch.
2. Add or edit content in the appropriate category directory.
3. Check that filenames, frontmatter, and content follow the category's documented format.
4. Open a pull request against `main` and describe the content change.

You do not need to modify or run the jargons.dev application to contribute dictionary content. The in-app editor is being updated to submit contributions to this repository; until that integration is available, submit a pull request here.

## Publishing

After content is merged into `main`, the website's deployment process will fetch this repository and build the updated content. Content pull requests do not change the website application itself.
