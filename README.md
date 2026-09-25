# scketamine.com

The landing page at `scketamine.com`. Two links out to the clinic sites, and
nothing else — no forms, no backend, no data.

**Deliberately separate from the clinical system.** The patient records app is a
different repository, a different Google Cloud project and a different domain
(`app.scketamine.com`). Nothing here touches it, and nothing here should ever
hold patient information.

## Deploying

Push to `main`. GitHub Pages serves it.

## The design is inherited, not invented

Both clinic sites set Montserrat on white and differ only by accent — Charleston
`#30A9DD`, Columbia `#6EA595`. This page uses both, one per card, which is the
whole job of a chooser. The wordmarks are the clinics' own, copied here rather
than hotlinked so a redesign on either site cannot break this page.
