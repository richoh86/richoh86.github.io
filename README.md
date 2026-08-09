# richoh86.github.io

The user-site root for <https://richoh86.github.io/>. It exists for two reasons.

## 1. `app-ads.txt`

AdMob and other ad buyers resolve an app's App Store marketing URL down to its
**registrable domain** and look for `/app-ads.txt` there. Because `github.io` is
on the Public Suffix List, that domain is `richoh86.github.io` — so the file has
to sit at the root, not under `blink-sort-site/`. Only a repository named
`richoh86.github.io` serves that path.

One file covers every app published under this account.

    google.com, pub-4726690883884969, DIRECT, f08c47fec0942fa0

`pub-4726690883884969` is the AdMob publisher ID; `f08c47fec0942fa0` is Google's
fixed certification authority ID and is the same for every publisher.

Adding another ad network later means adding one more line, not replacing this
one. Keep it plain text with no HTML wrapper — a crawler that receives a 404
page or a redirect treats the app as unverified.

Google re-crawls on its own schedule, so a change here can take a day or two to
show up as "authorized" in AdMob.

## 2. A landing page

`index.html` links to the per-app sites, which each carry their own support page
and privacy policy. Those live in separate repositories (`blink-sort-site`,
`tether-site`, …) and are unaffected by anything here.
