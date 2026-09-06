# Postal Media website

A simple static website for Postal Media and the Content app.

Files:
- `index.html` - company and product landing page
- `privacy.html` - Privacy Policy for Content
- `styles.css` - responsive styling
- `site.js` - tiny footer-year script
- `assets/` - provided Postal Media and Content artwork
- `_redirects` - forces HTTP traffic to HTTPS when deployed on Netlify
- `_headers` - adds common security headers when deployed on Netlify

Deploy the folder as a static site. No build step is required.

## HTTPS

The site is written to use HTTPS URLs and contains no insecure external assets.
The included `_redirects` and `_headers` files configure HTTPS enforcement and security headers on Netlify.
If you use another host, enable its automatic TLS/SSL certificate for `postalmedia.io` and configure an HTTP-to-HTTPS redirect there. The hosting provider is what actually terminates HTTPS; HTML alone cannot create the certificate.

Privacy policy URL:
`https://www.postalmedia.io/privacy.html`

Privacy contact:
`help@postalmedia.io`
