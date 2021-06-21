# Recipes

This repository contains a list of personal recipes and the source-code to
render them on a website.

You can view it in action at https://rezepte.bastian-oppermann.de/ (Disclaimer:
All recipes are in German).

## Format

The markdown recipe must have the following format:

```markdown
# Recipe Title

A description of the recipe (or even better an image).

## Ingredients

A list with all ingredients. Can use all markdown feature including "smaller"
headings.

## Instructions

A list with the instructions. Can use all markdown feature including "smaller"
headings.
```

The titles for ingredients and the instructions are not fixed and can be for
example in your local language. Only the order matters.

There must be exactly one `h1` header and two `h2` headers.

## Why?

I wanted to organize my personal recipes and had the following requirements:

### The recipes should be in a future-proof format

This means no 3rd-party app or program, since these might be discontinued. In
the best case, this means that I would have to migrate all my recipes to another
place. In the worst case, this means that I lose all my recipes unless I create
backups. Usually these kind of apps and programs offer a "Convert to PDF"
option, that could serve as a backup. However, this would mean, that I have to
export very often (for every newly created recipe or when updating an existing
one).

=> Markdown is simple and is likely to stick around for a very long time. After
all, it's just plain text.

The website itself is trying to be as simple as possible. It uses plain
JavaScript to render the markdown and plain CSS for styling. Dependencies are
kept to a minimum and included with reliable CDNs.

### The recipes should be accessible on mobile but also printable

This means, that plain markdown is not enough. Of course, you could render and
print it with an existing formatter, but these are not optimized for recipes.