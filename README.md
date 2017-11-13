# Creating A New October CMS Theme

This is based on the [Sitepoint][spa] tutorial and the [official][ood] article
about creating October CMS themes.

The active theme (there can only be one, cue lightning strike) is specified by
the `activeTheme` parameter in `config/cms.php` or using the Theme Selector in
the back-end system. The back-end choice overrides the parameter in `cms.php`.

## Structure of a theme folder

Themes are stored in the `/themes` directory, and contain `pages`, `partials`,
`layouts`, and `content` which can have one level of subdirectories each. The
`assets` subdirectory is also needed but can have any nesting structure.

`Pages` give style to the individual pages in a theme. `Partials` are reusable
HTML markup chunks. `Layouts` define the structure of a page, and `content` is
all the text/HTML/Markdown you may want to edit apart from the layout.

## Basic breakdown of a theme file

There are three sections in a theme file: configuration, PHP, and markup. This
means theme files could look very similar unless you look carefully at each of
the configuration sections to see what part of the site is being styled here.

This makes "porting" styles between types (partial, page, layout, component) a
breeze, since you can just copy files from folder to folder and edit them. But
I'm not sure if anyone would want to do that.

### Configuration

This first section describes the template to the CMS.

### PHP

This second section will be wrapped inside a cached PHP class, so here we have
to use functions or the `use` keyword.

### Markup

October uses the [Twig template engine][tte] from Symfony.

[spa]: https://www.sitepoint.com/build-octobercms-theme/
[ood]: https://octobercms.com/docs/cms/themes#introduction
[tte]: http://twig.sensiolabs.org/documentation
