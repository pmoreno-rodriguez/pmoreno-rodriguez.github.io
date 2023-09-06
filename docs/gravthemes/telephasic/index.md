# Tutorial for Telephasic Theme

## Default Options

Telephasic comes with a few default options that can be set site-wide.  These options are:

```yaml
production-mode:              # In production mode, only minified CSS is used. When disabled, nested CSS are enabled
favicon:                      # Choosse your own favicon
logo:                         # A custom logo rather than the default (see below)  
themeSlogan:                  # Custom text for slogan
blog-page: '/blog'            # The route to the blog listing page, useful for a blog style layout
featuredposts:                # Enable/Disable featured posts in right sidebar
featuredposts_category:       # Select category name for featured posts (configured in taxonomies)
featuredposts_number:         # The number of featured posts will be displayed on the right sidebar
hero_title:                   # Title for hero section in Homepage
hero_subtitle:                # Subtitle for hero section in Homepage
hero_button_text:             # Button text for hero section in Homepage
hero_button_url:              # Button URL for hero section in Homepage
contact_enabled:              # Enable/Disable contact form in Homepage
contact_title:                # Title for contact form in Homepage
contact_subtitle:             # Subtitle for contact form in Homepage
copyright_author:             # Copyright author information for contact form in Homepage
copyright_rights:             # Copyright text for contact form in Homepage
social_enabled:               # Enable/Disable social icons in footer
```
To make modifications, you can copy the `user/themes/telephasic/editorial.yaml` file to `user/config/themes/` folder and modify, or you can use the admin plugin.

> [!WARNING]
> NOTE: Do not modify the `user/themes/telephasic/telephasic.yaml` file directly or your changes will be lost with any updates

## Custom Logo

To add a custom logo, you should put the log into the `user/themes/telephasic/images/logo` folder.  Standard image formats are support (`.png`,`.jpg`, `.gif`, `.svg`, etc.).  Then reference the logo via the YAML like so:

```yaml
logo:
    - name: 'my-custom-logo.png'   
```
Alternatively, you can you use the drag-n-drop "Custom Logo" field in the Telephasic theme options.

