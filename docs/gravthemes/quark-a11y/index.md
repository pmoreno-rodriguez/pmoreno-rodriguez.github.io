# Quark-A11y Theme

**Quark-A11y** is a fork of the [Quark theme for Grav CMS](http://github.com/getgrav/grav), focused on improving **accessibility** while staying as faithful as possible to the original theme.  
This version introduces improved **ARIA labels** and more semantic HTML markup to provide a better experience for users relying on assistive technologies.  
Additionally, the **Spectre.css** framework has been updated to version **0.5.9**.

## Features

* Lightweight and minimal for optimal performance  
* **Spectre.css v0.5.9**  
* Improved HTML semantics and ARIA label support for better accessibility  
* Fully responsive with full-page mobile navigation  
* SCSS-based CSS source files for easy customization  
* Built-in support for on-page navigation  
* Multiple page template types  
* Fontawesome icon support  

### Supported Page Templates

* Default view template `default.md`
* Error view template `error.md`
* Blog view template `blog.md`
* Blog item view template `item.md`
* Modular view templates: `modular.md`
  * Features Modular view template `features.md`
  * Hero Modular view template `hero.md`
  * Text Modular view template `text.md`
  * Note: Gallery Modular view template `gallery.md` only works in concert with premium plugin [Lightbox Gallery](https://getgrav.org/premium/lightbox-gallery/docs)

# Installation

Installing Quark-A11y can be done in two ways. The **GPM (Grav Package Manager)** method is the quickest and easiest, but you can also install it manually using a zip file. 

## GPM Installation (Preferred)

The simplest way to install this theme is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm) through your system's Terminal (also called the command line).  From the root of your Grav install type:

    bin/gpm install quark-a11y

This will install the Quark-A11y theme into your `/user/themes` directory within Grav. Its files can be found under `/your/site/grav/user/themes/quark-a11y`.

## Manual Installation

To install this theme, just download the zip version of this repository and unzip it under `/your/site/grav/user/themes`. Then, rename the folder to `quark-a11y`. You can find these files either on [GitHub](https://github.com/pmoreno-rodriguez/grav-theme-quark-a11y) or via [GetGrav.org](http://getgrav.org/downloads/themes).

You should now have all the theme files under

    /your/site/grav/user/themes/quark-a11y

## Default Options

Quark-A11y comes with a few default options that can be set site-wide.  These options are:

```yaml
enabled: true                 # Enable the theme
production-mode: true         # In production mode, only minified CSS is used. When disabled, nested CSS with sourcemaps are enabled
grid-size: grid-lg            # The max-width of the theme, options include: `grid-xl`, `grid-lg`, and `grid-md`
header-fixed: true            # Cause the header to be fixed at the top of the browser
header-animated: true         # Allows the fixed header to resize to a smaller header when scrolled
header-dark: false            # Inverts the text/logo to work better on dark backgrounds
header-transparent: false     # Allows the fixed header to be transparent over the page
sticky-footer: true           # Causes the footer to be sticky at the bottom of the page
blog-page: '/blog'            # The route to the blog listing page, useful for a blog style layout with sidebar
custom_logo:                  # A custom logo rather than the default (see below)  
custom_logo_mobile:           # A custom logo to use for mobile navigation
```

To make modifications, you can copy the `user/themes/quark-a11y/quark-a11y.yaml` file to `user/config/themes/` folder and modify, or you can use the admin plugin.

> NOTE: Do not modify the `user/themes/quark-a11y/quark-a11y.yaml` file directly or your changes will be lost with any updates

## Custom Logos

To add a custom logo, you should put the log into the `user/themes/quark-a11/images/logo` folder.  Standard image formats are support (`.png`,`.jpg`, `.gif`, `.svg`, etc.).  Then reference the logo via the YAML like so:

```yaml
custom_logo:
    - name: 'my-logo.png'
custom_logo_mobile:
    - name: 'my-mobile-logo.png'    
```

Alternatively, you can you use the drag-n-drop "Custom Logo" field in the Quark-A11y theme options.

## Page Overrides

Quark-A11y has the ability to allow pages to override some of the default options by letting the user set `body_classes` for any page.  The theme will merge the combination of the defaults with any `body_classes` set. For example:

```yaml
body_classes: "header-dark header-transparent"
```

On a particular page will ensure that page has those options enabled (assuming they are false by default).

## Hero Options

The hero template allows some options to be set in the page frontmatter. This is used by the modular `hero` as well as the blog and item templates to provide a more dynamic header.

```yaml
hero_classes: text-light title-h1h2 parallax overlay-dark-gradient hero-large
hero_image: road.jpg
hero_align: center
```

The `hero_classes` option allows a variety of hero classes to be set dynamically these include:

* `text-light` | `text-dark` - Controls if the text should be light or dark depending on the content
* `title-h1h2` - Enforced a close matched h1/h2 title pairing
* `parallax` - Enables a CSS-powered parallax effect
* `overlay-dark-gradient` - Displays a transparent gradient which further darkens the underlying image
* `overlay-light-gradient` - Displays a transparent gradient which further lightens the underlying image
* `overlay-dark` - Displays a solid transparent overlay which further darkens the underlying image
* `overlay-light` - Displays a solid transparent overlay which further darkens the underlying image
* `hero-fullscreen` | `hero-large` | `hero-medium` | `hero-small` | `hero-tiny` - Size of the hero block

The `hero_image` should point to an image file in the current page folder.

## Features Modular Options

The features modular template provides the ability to set a class on the features, as well as an array of feature items.  For example:

```yaml
class: offset-box
features:
    - header: Crazy Fast
      text: "Performance is not just an afterthought, we baked it in from the start!"
      icon: fighter-jet
    - header: Easy to build
      text: "Simple text files means Grav is trivial to install, and easy to maintain"
      icon: database
    - header: Awesome Technology
      text: "Grav employs best-in-class technologies such as Twig, Markdown &amp; Yaml"
      icon: cubes
    - header: Super Flexible
      text: "From the ground up, with many plugin hooks, Grav is extremely extensible"
      icon: object-ungroup
    - header: Abundant Plugins
      text: "A vibrant developer community means over 200 themes available to download"
      icon: puzzle-piece
    - header: Free / Open Source
      text: "Grav is an open source project, so you can spend your money on other stuff"
      icon: money 
```

## Text Modular Options

The text box provides a single option to control if any image found in the page folder should be left or right aligned:

```yaml
image_align: right
```

# Demo page

[https://quark-a11y.pmdesign.dev](https://quark-a11y.pmdesign.dev)

# Documentation 

You can read extra documentation of Future2021 Theme at [https://pmoreno-rodriguez.github.io/#/./gravthemes/quark-a11y/index](https://pmoreno-rodriguez.github.io/#/./gravthemes/quark-a11y/index). This is [Spanish document site for Future2021 Theme](https://pmdesign.dev/temas/quark11-a11y)