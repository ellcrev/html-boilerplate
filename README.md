# html-boilerplate

Optimal HTML Boilerplate for Modern Web Apps

Replace any `@inject-**` with the proper content that belongs in that section.

```html
<!DOCTYPE html>
<html lang="@inject-lang">
  <head>
    <!-- Compatibility Tags -->
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />

    <!-- Search Engine Optimization Tags -->
    <meta name="description" content="@inject-description" />
    <meta name="keywords" content="@inject-keywords" />
    <meta name="author" content="@inject-author" />

    <!--  Open Graph Meta Tags -->
    <meta property="og:title" content="@inject-og-title" />
    <meta property="og:description" content="@inject-og-description" />
    <meta property="og:image" content="@inject-og-image" />
    <meta property="og:url" content="@inject-og-url" />
    <meta property="og:type" content="@inject-og-type" />

    <!-- Progressive Web App Tags -->
    <meta name="theme-color" content="@inject-theme-color" />
    <link rel="manifest" href="@inject-manifest" />

    <!-- Apple-Specific Tags -->
    <link rel="apple-touch-icon" href="@inject-apple-touch-icon" />
    <meta
      name="apple-mobile-web-app-status-bar"
      content="@inject-apple-mobile-web-app-status-bar"
    />
    <meta
      name="apple-mobile-web-app-title"
      content="@inject-apple-mobile-web-app-title"
    />

    <!-- Microsoft-Specific Tags -->
    <meta
      name="msapplication-TileColor"
      content="@inject-msapplication-TileColor"
    />
    <meta
      name="msapplication-TileImage"
      content="@inject-msapplication-TileImage"
    />

    <!-- Twitter Card Tags -->
    <meta name="twitter:card" content="@inject-twitter-card" />
    <meta name="twitter:title" content="@inject-twitter-title" />
    <meta name="twitter:description" content="@inject-twitter-description" />
    <meta name="twitter:image" content="@inject-twitter-image" />

    <!-- Favicon Link -->
    <link rel="icon" type="image/x-icon" href="@inject-favicon-ico" />

    <!-- App, Layout, and Page Styles -->
    <link rel="stylesheet" href="@inject-app-css" />
    <link rel="stylesheet" href="@inject-layout-css" />
    <link rel="stylesheet" href="@inject-page-css" />

    <title><!-- @inject-title --></title>
  </head>
  <body>
    <!-- @inject-body -->
    <script src="@inject-app-js" type="text/javascript"></script>
    <script src="@inject-layout-js" type="text/javascript"></script>
    <script src="@inject-page-js" type="text/javascript"></script>
  </body>
</html>
```
