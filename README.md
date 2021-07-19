# 👨‍🍳 Recipes

![Example](/.github/example.png)

A list of personal recipes in markdown format and the source-code to render them
on a website.

You can view it in action here: [Burger recipe][smashed-burger]
(*Disclaimer: All recipes are in German*). Many of the recipes are
work-in-progress and will be improved over time.

While this project is for my personal use, you can very easily use it to manage
your own recipes. Just fork it, setup GitHub Pages, and swap out the recipes for
your own.

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
all, it's just plain text. Even if this tool stops working, I still have the
markdown files.

The website itself is trying to be as simple as possible. It uses plain
JavaScript to render the markdown and plain CSS for styling. Dependencies are
kept to a minimum and directly download to the `libs` folder (no CDN or package
manager).

### The recipes should be accessible on mobile but also printable and easy to share

This means, ideally a website and not some document like Word or OpenOffice.

It also means that plain markdown is not enough. Of course, you could render
and print it with an existing formatter but these are not optimized for recipes.

## Format

### Recipes

While recipes are 100% markdown, this does not mean, that every markdown
document is compatible. Recipes must follow a specific format that looks like
the one shown below:

```markdown
# Recipe Title

A description of the recipe (or even better an image).

## Ingredients

A list with all ingredients. Can use all markdown feature including "smaller"
headings.

## Instructions

A list with the instructions. Can use all markdown feature including "smaller"
headings.

## Images

A list with images (optional).
```

The titles for ingredients and the instructions are not fixed and can be for
example in your local language. Only the order matters.

There must be exactly one `h1` header and two to three `h2` headers. If the
markdown does not fullfil these requirements, the script might not render the
recipe correctly or maybe even not at all.

### Recipe list

The recipe list is rendered from the `recipes.md` file and can be in any format
you want. The website just renders the markdown without any special treatment.

## Deployment

You can just serve all files of the repository with a webserver and it will
work. The easiest way to do this, is to use 
[GitHub Pages](https://pages.github.com/) for it. This will work out-of-the-box
(you just have to remove/replace the `CNAME` file).

[smashed-burger]: https://rezepte.bastian-oppermann.de/?recipe=smashed-burger