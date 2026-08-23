# scoutfeed (demo)

The live demo behind [amir-hackett.github.io/scoutfeed](https://amir-hackett.github.io/scoutfeed/).

**Sample data only.** The page ships empty. You name the things you care about,
and it queries [Hacker News](https://hn.algolia.com/api) and
[The Guardian](https://open-platform.theguardian.com/) from your browser, ranks
what comes back by match strength and freshness, and marks the three it would
have texted you. Interests live in `localStorage` and are never sent anywhere.

This repository is a single self-contained `index.html` — no build, no
dependencies, no server, no private keys. (The Guardian key is the literal
string `test`, their documented open key for exactly this.)

## What the real one does

The real scoutfeed reads a few dozen RSS feeds on a schedule, scores each story
against a long-lived interest profile, texts the top three, and keeps everything
else on a page so nothing gets missed. This demo reproduces the shape of that in
a page that can hold no secrets.
