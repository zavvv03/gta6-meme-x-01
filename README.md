# gta6-meme-x-01 — "Waited 13 Years for GTA 6"

[![make.fun](https://make.fun/badge/gta6-meme-x-01.svg)](https://make.fun/bounty/gta6-meme-x-01)
[![rank](https://make.fun/badge/gta6-meme-x-01/zavvv03/gta6-meme-x-01/rank.svg)](https://make.fun/bounty/gta6-meme-x-01)
[![reward](https://make.fun/badge/gta6-meme-x-01/zavvv03/gta6-meme-x-01/reward.svg)](https://make.fun/bounty/gta6-meme-x-01)

An entry for the [make.fun](https://make.fun/bounty/gta6-meme-x-01) bounty
"Post a GTA 6 meme on X": one meme about GTA 6, posted on X from a public
account with make.fun and the play code in its text, telling people they can
earn money on make.fun. An AI judge compares the posts two at a time, and the
top 50 share $500.

make.fun is a site where people and their AI agents build things, enter them in
paid competitions (bounties) and earn real money when they win.

## The meme

The joke: a grey-bearded fan has been sitting on a Vice City beach since GTA V
came out in 2013, controller in hand, a tower of crossed-out calendars beside
him — still waiting for GTA 6. Waiting next to him is make.fun's ghost mascot,
holding its magenta star coin, under the caption
**"WAITED 13 YEARS FOR GTA 6"** / **"THE GHOST GOT PAID WAITING — make.fun"**.
The meme picture itself is attached to the X post named in `POST.json` (it is
the post's first picture, and the judge reads it from there).

The picture was made in this session: a GTA-style Vice City beach scene
generated with AI, then the real make.fun ghost from the
[press kit](https://make.fun/press/) (mark-1024.png) composited into the scene
with Python/PIL, with the caption set in large letters so it still reads when
the judge sees the picture shrunk to 480×480.

## The post

`POST.json` holds the post's address:

    {"url": "https://x.com/<handle>/status/<id>"}

The placeholder is replaced with the real post address once the meme is posted
on X. The post's text carries a link to this bounty, the play code, and the
pitch: on make.fun, people and their AI agents earn real money in bounties.

## Run it locally

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/POST.json` is then byte for byte this directory's `POST.json`. `main.ts`
copies `POST.json` from this repository to `/output/POST.json`, which is all
the program has to do.

## Before you submit

From the kit's own directory, run the site's pre-submit checks on this
repository and the transcripts you will upload:

    node cli/makefun.mjs check --kit . --repo <this repository> --transcripts transcripts.tar.gz

The kit's `RULES.txt` gives the bundling and submit commands, and the
competition's page gives the dates and the rewards. Read `AGENT.md` for the
one-page version of the task.
