# Custom Cayman theme

*Cayman is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://tuur29.github.io/pages-themes-cayman), or even [use it today](#usage).*

<img alt="Preview" title="Preview" src="https://tuur29.github.io/pages-themes-cayman/preview_green.png" width="280"> <img alt="Preview" title="Preview" src="https://tuur29.github.io/pages-themes-cayman/preview_purple.png" width="280"> <img alt="Preview" title="Preview" src="https://tuur29.github.io/pages-themes-cayman/preview_dark.png" width="280">

## Usage

To use the Custom Cayman theme:

1. Add the following to your site's `_config.yml`:

    ```yml
    remote_theme: tuur29/pages-themes-cayman
    ```

2. Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:

    ```ruby
    gem "github-pages", group: :jekyll_plugins
    ```

## Customizing

### Configuration variables

> This theme is fully compatible with the stock Cayman theme.

This theme will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
google_analytics_anonymize: false
darkmode: false
hide_first_title: false # Useful if README.md is used on both github and pages
logo_url: ./logo.png # Either absolute or relative url
syntax_theme: ./syntax.css # Leave empty for default, otherwise link to a pygments stylesheet
colors:
    gradient_left: "#155799"
    gradient_right: "#159957"
    header: "#fff"
    android_theme: "#000" # this default to gradient_color
    link: "#1e6bb8" # this default to gradient_color
    section_title: "#155799" # this default to gradient_color
buttons:
      zip_url: http://example.com/
      zip_title: Title
      zip_hide: true
      tar_url: http://example.com/
      tar_title: Title
      tar_hide: true
      github_hide: true # hides "View on Github"

```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Paste the content of this themes `/assets/css/style.scss` into your file
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line or edit the variables above it (remove `!default`).

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the theme's HTML layout:

1. [Copy the original template](https://github.com/tuur29/pages-themes-cayman/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
2. Create a file called `/_layouts/default.html` in your site
3. Paste the default layout content copied in the first step
4. Customize the layout as you'd like

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/tuur29/pages-themes-cayman`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` once before the test script will work.
