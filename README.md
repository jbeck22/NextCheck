# NextCheck

Public marketing site, support page, and privacy policy for **NextCheck**, a
paycheck-cycle budgeting app for iPhone, iPad, and web. Plain static HTML/CSS
(no build step, no Jekyll — `.nojekyll` disables GitHub Pages' default
processing so what's committed is exactly what's served).

- Currently live at: https://jbeck22.github.io/NextCheck/
- Moving to: **nextcheck.net** once the domain is purchased and DNS is
  pointed at GitHub Pages (a `CNAME` file is already in place). GitHub Pages
  keeps serving the default `github.io` URL alongside any custom domain, so
  this switch doesn't break anything already live.
- The actual app lives elsewhere: [nextcheck-ios](https://github.com/jbeck22/nextcheck-ios)
  (private, native app source) and [nextcheck-web](https://github.com/jbeck22/nextcheck-web)
  (private, the Bills-only companion web app — planned to move to
  `my.nextcheck.net` once the domain is live).

## ⚠️ These URLs are registered with Apple, live, during App Review

`index.html` (Support URL) and `privacy-policy.html` (Privacy Policy URL) are
the exact URLs on file in App Store Connect for the submitted app. Don't
remove or break either path, and keep the Support section's contact info and
account-deletion instructions genuinely present on `index.html` even as the
page evolves — a marketing-first homepage with a real support/contact section
is normal and satisfies Apple's requirement, but a homepage with *no* support
info would not.

## Structure

```
index.html            Marketing landing page (hero, features, pricing, support)
privacy-policy.html   Privacy policy (verbatim legal text, same page chrome)
assets/style.css       Shared stylesheet, brand colors match the app's Theme.swift
assets/logo.png         App icon, reused as site favicon/brand mark
assets/screenshots/     Resized copies of the App Store screenshots
CNAME                  nextcheck.net -- GitHub Pages custom domain marker
```

All internal links are relative (`index.html`, `index.html#features`, not
`/` or `/#features`) so the site works correctly both at the current
`github.io/NextCheck/` subpath and at the future `nextcheck.net` root --
no changes needed when the domain switches over.

## Updating

Just edit the HTML directly and push to `main` -- GitHub Pages redeploys
automatically. To update the privacy policy, edit the legal text in
`privacy-policy.html` directly (there's no separate Markdown source anymore)
and bump the effective date at the top.
