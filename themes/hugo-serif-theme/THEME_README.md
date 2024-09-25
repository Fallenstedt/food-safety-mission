## Configuring Theme

### Logo

You can edit the logo from the `config.toml`

```toml
# config.toml

  [params.logo]
    mobile = "images/logo/logo-mobile.svg"
    mobile_height = "36px"
    desktop = "images/logo/logo.svg"
    desktop_height = "36px"
    alt = "Serif - A Hugo Business Theme"
```

### Favicon

You can edit the favicon from the `config.toml`

```toml
# config.toml

[params]
  google_analytics_id = "UA-XXX-1"
  google_tag_manager_id = ""
  favicon = "favicon-32x32.svg"
```

### Fonts

This theme uses Google fonts. You can change the google font in the `config.toml` - These fonts are injected into the `style.scss` as SCSS variables.

```toml
# config.toml

  [params.fonts]
    # sets the google font link in layouts/partials/google-fonts.html
    google_fonts = 'https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Source+Sans+Pro:wght@400;700&display=swap'
    heading = "Playfair Display"
    base = "Source Sans Pro"
```

### Colors

You can edit the themes main colors in the `config.toml`. These colors are injected into the `style.scss` as SCSS variables.

```toml
#config.toml

  [params.colors]
    primary = "#f24088"
    black = "#2f2f41"
    white = "#ffffff"
    white_offset = "#f6f7ff"
    grey = "#5C5A5A"
```

### Intro Image

List pages such as the homepage, services and team can have a Intro image.

```yml
# content/_index.md
---
intro_image: "https://source.unsplash.com/wOGhHamMqLc"
intro_image_absolute: false
intro_image_hide_on_mobile: true
---
```

While this themes default content uses illustrations, its easy to change the image to a photo and it will still look great.

the front-matter field `intro_image_absolute: true` let's illustrations "break out" (in CSS terms, it uses `position: absolute`) of the grid and is an intended stylistic effect. When using photos or normal images it's recommended to set this field to false and the photo will align with the grid. See `content/team/_index.md` for an example.

### Google Analytics

Put your Google Analytics ID in the `google_analytics_id` field in the `config.toml` - Also supports Google Tag Manager. When your site is running locally using `hugo server` the GA tag is not injected. This prevents polluting your real data.

```toml
# config.toml

[params]
  google_analytics_id = "UA-XXX-1"
  google_tag_manager_id = ""
```

You can also set the Google Analytics ID using a [Netlify environment variable](https://docs.netlify.com/configure-builds/environment-variables/) `HUGO_GOOGLE_ANALYTICS_ID`

### Meta tags

A pages `<title>` is generated from the front-matter `meta_title` else it will use the `title` property. This allows you to have a different heading on the page to what is shown in the SEO title. See `content/_index.md` for an example.

The meta description field is generated from the front-matter `description`

OG meta data for Facebook and Twitter is also generated on a per page basis. The `image` field is used for the og:image for Twitter and Facebook.

You can configure og meta data global settings in the config.

```toml
# config.toml

  [params.seo]
    meta_twitter_site = "@zerostaticio"
    meta_twitter_creator = "@zerostaticio"
    meta_og_image = "https://www.zerostatic.io/theme/hugo-serif/hugo-serif-screenshot.png"
```

## License

- Don't create ports of this theme without asking me
- You can't re-distribute or re-sell this theme as your own template

## Credits

- Beautiful royalty free Illustrations by Icons8 - https://icons8.com/illustrations/style--pixeltrue
- Stock images by Unsplash - https://unsplash.com/
- Feature icons by Noun Project - https://thenounproject.com/

**More Hugo Themes by Zerostatic**

- [Hugo Hero](https://github.com/zerostaticthemes/hugo-hero-theme) - Open-source business theme
- [Hugo Whisper](https://github.com/zerostaticthemes/hugo-whisper-theme) - Open-source documentation theme
- [Hugo Serif](https://github.com/zerostaticthemes/hugo-serif-theme) - Open-source business theme
- [Hugo Winston](https://github.com/zerostaticthemes/hugo-winston-theme) - Open-source blog theme
- [Hugo Advance](https://www.zerostatic.io/theme/hugo-advance/) - Premium advanced multi page business & marketing theme
- [Hugo Paradigm](https://www.zerostatic.io/theme/hugo-paradigm/) - Premium landing page + site builder theme
- [Hugo Lever](https://www.zerostatic.io/theme/hugo-lever/) - Premium personal / bio theme
- [Hugo Shard](https://www.zerostatic.io/theme/hugo-lever/) - Premium SAAS / landing page theme

**Find hundreds more Hugo themes on Built At Lightspeed**

[<img alt="Built At Lightspeed Hugo themes directory screenshot" width="400px" src="https://www.zerostatic.io/images/builtatlightspeed-hugo-themes.jpg" />](https://builtatlightspeed.com/category/hugo)
