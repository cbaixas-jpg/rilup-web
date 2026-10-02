# rilup.com

The public site for **Rilup**, a social network where the only thing you can post is what you
capture live inside the app. No gallery, no uploads, nothing generated.

This repository holds the site only: landing page, manifesto, how it works, the waitlist form
and the legal pages. Static HTML and CSS, no framework, no build step, and no analytics or
tracking of any kind.

## Deploying

GitHub Pages serves `main` from the repository root, at the `rilup.com` custom domain set in
`CNAME`. Pushing to `main` publishes.

The pages are authored in the `web/` directory of the main Rilup repository, which is private,
and copied here to publish. Edit them there, not here, or the next copy will overwrite the
change.

## The app

The Android app, the backend and the capture-attestation pipeline live in a separate private
repository. Nothing in this one talks to them beyond two public endpoints: the waitlist insert
and the public post viewer.

The Supabase key embedded in the waitlist form is the anonymous key, public by design, the same
one shipped inside the app. What protects the data is the row-level security policy on the
table: it allows an insert and refuses every read.

---

Pahoehoe SpA, Chile
