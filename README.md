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

# Web Page Processing

1. Browser navigates to a website.
2. Server sends an HTML file.
3. Browser begins parsing HTML, and `window.document` emits `readystatechange` event where `readyState="loading"`.

- `<script>` (inline): Browser stops parsing, executes script to completion, then continues parsing.
- `<script>` (external): Browser stops parsing, downloads script, executes script to completion, then continues parsing.
- `<script defer>`: Browser adds script to its download queue (background), then continues parsing.
- `<img>, <link>, etc.`: Browser adds resource to its download queue (background), then continues parsing.

4. When finished parsing, `window.document` emits `readystatechange` event where `readyState="interactive"`.
5. Browser executes all `<script defer>` in the order they appeared in the html.
6. After executing all `<script defer>`, `window.document` emits the `DOMContentLoaded` event.
7. Once download queue is complete, `window.document` emits `readystatechange` where `readyState="complete"`.
8. Browser `window` emits the `load` event.

> `<script async>` is not recommended or covered as:
>
> - Execution time is unpredictable.
> - Can unintentionally interrupt HTML parsing.
