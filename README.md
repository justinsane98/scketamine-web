# scketamine.com

The landing page at **https://scketamine.com**. Two cards, two links out to the
clinic sites, and nothing else — no forms, no backend, no data.

Someone arrives here by mistyping, or from a link, and the only thing they want
is the clinic nearest them. The page is that question and its two answers.

## Deploying

```sh
firebase deploy --only hosting
```

That is the whole process. Firebase project: **`sc-ketamine-site`**, free Spark
plan, custom domain and TLS included.

If `firebase` is not found or behaves oddly, check the version — there may be an
old one on `PATH`:

```sh
firebase --version                              # should be 15.x or newer
~/.nvm/versions/node/v22.13.0/bin/firebase      # the known-good one
```

**GitHub Pages is deliberately disabled on this repo.** The page was deployed
there first while Firebase was blocked. The repo stays as the source of truth;
Pages stays off so it cannot compete for the domain.

## Deliberately separate from the clinical system

The patient records app is a different repository, a different Google Cloud
project (`ckc-app-production`) and a different domain
(`app.scketamine.com`). Nothing here touches it.

**Nothing in this repository should ever hold patient information.** It is a
public repo serving a public page.

## The design is inherited, not invented

Both clinic sites already set **Montserrat on white** and differ only by accent:

| | |
|---|---|
| Charleston | `#30A9DD` |
| Columbia | `#6EA595` |

This page uses both, one per card, which is the whole job of a chooser. The
wordmarks are the clinics' own, **copied in rather than hotlinked** — a redesign
on either site should not be able to break this page.

Each card carries two real links: a `tel:` number and the site. It was
originally one large anchor wrapping the whole card, which made the phone number
untappable — an anchor cannot contain another anchor, and a phone number on a
phone should dial.

## Two facts worth knowing

**`charlestonketamineclinic.com` does not exist.** The live Charleston site is
`charlestonketaminecenter.com`, which is what this links to.

**The two clinics name themselves inconsistently.** Columbia's own site refers to
the Charleston location as "Charleston Ketamine Clinic" in its footer, while
Charleston's site says "Center". This page uses each clinic's own wordmark, so
it shows whatever they call themselves.
