# Butler 
Butler is a clean, responsive theme for [zola](https://github.com/getzola/zola).

Demo: [See it in action](https://shaleenjain.com/butler)

## Contents

- [Installation](#installation)
- [Options](#options)
  - [Top menu](#top-menu)
  - [Title](#title)

## Installation
First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/shalzz/butler.git
```
and then enable it in your `config.toml`:

```toml
theme = "butler"
```

This theme provides an additional template `blog.html` that
paginates all the pages in a section.
To use it enable in your section frontmatter.

```
+++
template = "blog.html"
sort_by = "date"
paginate_by = 10
+++
```

All the three options above are required for the blog template to work properly.

## Options

### Top-menu
Set a field in `extra` with a key of `butler_nav_bar`:

```toml
# This is the default menu
butler_nav_bar = [
    {url = "$BASE_URL/blog", name = "Blog"},
]
```

If you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

### Title
The site title is shown on the header. As it might be different from the `<title>`
element that the `title` field in the config represents, you can set the `author.name`
instead.
