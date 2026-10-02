---
title: Privacy Policy
description: What the Nerdelandslaget Quizbot Discord bot stores, and how to have it deleted
---

# Privacy Policy — Nerdelandslaget Quizbot

**Last updated:** 2 October 2026

Quizbot is a non-commercial Discord bot that keeps a scoreboard for one
community. It tracks results from two daily browser puzzle games,
[GuessTheGame](https://guessthe.game) and
[Spillrulett](https://www.gamer.no/spillrulett), that members choose to share.

This policy explains exactly what the bot stores, why, and how to get it removed.

---

## Who runs this bot

Quizbot is operated by a private individual, not a company. It is not monetised
and has no users outside the community it was written for.

**Contact:** send a direct message to the bot's operator, or to any server
administrator, in the Nerdelandslaget Discord server. Deletion requests are
handled manually, normally within a few days.

---

## What the bot stores

### If you have opted in with `/bli-med`

| Data | Example | Why |
|---|---|---|
| Discord user ID | `123456789012345678` | Identifies your results |
| Discord display name | `Scrang4Chuck` | Shown on the scoreboards |
| Server (guild) ID | `570695643123427426` | Keeps servers separate |
| Game | `guessthegame` | Which puzzle |
| Puzzle number | `1432` | Prevents the same puzzle counting twice |
| Score | `3` | Guesses used, or stars earned |
| Result grid | `🟥🟨🟩` | Shown on the daily summary |
| Date played | `2026-10-02T12:00:00` | Groups results by day |
| Medals and badges | `gold, 2026-W40` | Weekly awards |

### If you have *not* opted in

If you post a recognisable game result in the tracked thread without having
opted in, the bot records **your Discord user ID, your display name, and the
time it first saw you** — and nothing else. No score is saved.

This exists for one reason: so the bot sends you the "you can join with
`/bli-med`" message once, and never pesters you again. You can have this record
deleted at any time (see below).

---

## What the bot does **not** store

The bot **does not store the text of your messages.** When you share a result,
it reads the message, extracts the puzzle number and the emoji result grid, and
discards everything else. Hashtags, links, and anything you wrote alongside the
result are never written to disk.

It also never stores or collects:

- Message IDs, message history, or any conversation content
- Direct messages
- Email addresses, real names, IP addresses, or payment details
- Presence, status, voice activity, or the server's member list
- Messages from any channel other than the one thread an administrator
  registered with `/init`
- Messages from any server that has not registered a thread

---

## How the data is used

Only to produce the scoreboards and statistics the bot exists for: daily
summaries, weekly and monthly leaderboards, weekly medals, and the `/statistikk`
and `/toppliste` commands.

Your data is **never**:

- sold, rented, or shared with anyone
- used to train machine-learning or AI models
- sent to any analytics, advertising, or third-party service
- used for moderation, profiling, or anything unrelated to quiz scores

Results are visible to other members of the same Discord server, because that is
what a scoreboard is. They are not published anywhere else.

---

## Where the data is kept

In a single SQLite database file on a private virtual server rented from
Hetzner, located in Finland, within the EU/EEA. The server is accessible only
to the bot's operator via SSH key.

The database is not encrypted at rest beyond the protections the hosting
provider applies to its own infrastructure.

---

## How long it is kept

Results are kept for as long as the scoreboard is running, because the bot
reports all-time statistics and yearly rankings. There is no automatic deletion.

Your data is removed when you ask for it to be removed.

---

## Your choices

| What you want | How |
|---|---|
| Start being tracked | `/bli-med` |
| Stop being tracked | `/forlat` — new results are ignored, **existing history is kept** |
| Delete everything | Ask a server administrator to run `/fjern @you`, or contact the operator |
| See what is stored about you | `/statistikk` shows your records, or ask the operator |

`/fjern` is immediate and permanent. It deletes your results, medals, badges and
your user record — every row the bot holds about you.

If you would rather not go through a server administrator, message the operator
directly on Discord. Requests are handled manually, normally within a few days.

---

## Children

The bot is not directed at children and collects nothing that identifies age.
Discord requires its users to be at least 13 years old.

---

## Changes

Any change to this policy will be published at this URL with an updated date at
the top. Material changes will be announced in the Discord server.

---

## Norsk sammendrag

Quizbot lagrer **ikke** teksten i meldingene dine. Når du deler et resultat
leser boten ut puslespillnummeret og emoji-rutenettet, og forkaster resten —
hashtagger, lenker og alt annet du skriver blir aldri lagret.

For deg som har meldt deg på med `/bli-med` lagres: Discord-ID, visningsnavn,
server-ID, hvilket spill, puslespillnummer, poengsum, emoji-rutenettet, dato, og
medaljer.

Har du **ikke** meldt deg på, men poster et resultat i tråden, lagres kun
Discord-ID, visningsnavn og tidspunkt — slik at boten bare sender deg
invitasjonsmeldingen én gang. Ingen poengsum lagres.

Dataene selges aldri, deles aldri med tredjeparter, og brukes aldri til å trene
KI-modeller. De ligger i en SQLite-database på en privat server.

- `/bli-med` — start sporing
- `/forlat` — stopp sporing (historikken beholdes)
- `/fjern @deg` (admin) — sletter alt boten har om deg, permanent

Spørsmål eller sletteforespørsler: send en direktemelding til operatøren
eller en administrator i Discord-serveren.
