# RoyalTransfer EU Image Hosting

This repository hosts static image files for the [RoyalTransfer EU](https://www.royaltransfer.eu) website. It's deployed to the subdomain `files.royaltransfer.eu` on Netlify.

## Purpose

This repository serves as a dedicated image CDN for the main RoyalTransfer website. It's designed to:

- Host image assets in various formats (WebP, PNG, etc.)
- Serve images efficiently with proper cache headers
- Block search engine indexing to avoid duplicate content issues

## Structure

```
/
├── assets/           # Image files directory
├── index.html        # Simple landing page
├── 404.html          # Custom 404 page
├── robots.txt        # Search engine directives
├── style.css         # Minimal styling
└── netlify.toml      # Netlify configuration
```

## Usage

When adding images to the main website, use the following format:

```html
<img src="https://files.royaltransfer.eu/assets/image-name.webp" alt="Descriptive alt text">
```

For responsive images:

```html
<picture>
  <source srcset="https://files.royaltransfer.eu/assets/image-mobile.webp" media="(max-width: 768px)">
  <img src="https://files.royaltransfer.eu/assets/image-desktop.webp" alt="Descriptive alt text">
</picture>
```

## Image Access

All images placed in the `/assets/` directory will be directly accessible via URLs like:
```
https://files.royaltransfer.eu/assets/image-name.webp
https://files.royaltransfer.eu/assets/image-name.png
```

These files are configured with proper cache headers for optimal performance.

## SEO Considerations

This subdomain is intentionally not indexed by search engines to avoid duplicate content issues. All images should have proper alt text when used on the main site.