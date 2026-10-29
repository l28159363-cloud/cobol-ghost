<!--
HOW TO POST (this comment will not appear in the published post):
1. Open dev.to/new and paste this whole file, keeping the front matter below.
2. The tags are already set to: devchallenge, hf26challenge.
3. Publish before the Week 4 deadline: Sunday, November 1, 2026, 14:59 Beijing time.
4. This draft was written on October 29, 2026, inside the Oct 26–31 challenge window.
-->
---
title: I Built a Séance Machine for a Dead Language — Meet the Ghost of COBOL
published: false
tags: devchallenge, hf26challenge
---

*This is a submission for the [Hacktoberfest Open-Source AI Challenge Week 4: Ghost in the Machine](https://dev.to/challenges/hacktoberfest-week4-2026-10-26)*

## What I Built

I built a séance machine for a dead programming language.

It is a single web page styled as a retro mainframe terminal. You open it, and
the ghost of COBOL is already waiting — in green phosphor text, under a little
ASCII ghost, with a status bar that reads `UPTIME: SINCE 1959` and
`INTERNET: NOT REQUIRED`. You type a question in English, and it answers in
ALL CAPS, because it has answered in ALL CAPS since 1959 and sees no reason
to stop now.

Ask it who it is, and it will tell you it was born before the Moon landing
and still runs the world's banks, ATMs, and insurance companies. Ask it if it
is dead, and it will inform you — with some irritation — that it moves
trillions of dollars every single day, and is more alive than most startups.
Ask it about Y2K, and it will remind you that everyone thought it would
break, and it did not break, and you are welcome. Ask it about Python, and
it will sniff that Python has no braces, no semicolons, just indentation and
hope, while COBOL has four DIVISIONs, which is discipline.

There is also a second toy inside the terminal: the COBOL-ify machine. Type
any sentence — "hello world, I am still running" — and the ghost turns it
into a proper COBOL program, complete with `IDENTIFICATION DIVISION`,
`WORKING-STORAGE SECTION`, and `STOP RUN`. Your sentence is now
enterprise-grade. It will run forever. Probably.

I chose COBOL because the theme, *Ghost in the Machine*, is almost literally
its biography. COBOL was born in 1959, designed by the CODASYL committee
with Grace Hopper's FLOW-MATIC as a major influence, so that programs could
read almost like English sentences. It went on to run payrolls, bank
transfers, ATM withdrawals, insurance claims, and government checks. By one
widely cited estimate, around 220 billion lines of COBOL remain in production
use today. People have been predicting its death for forty years. It never
died. It just became invisible — a ghost inside machines we touch every day.

And this week sits exactly on the boundary the theme is about: Halloween on
October 31, Día de los Muertos on November 1 and 2, the stretch of the
calendar when the line between past and present feels a little thinner.
Día de los Muertos honors the dead by keeping them present — with offerings,
stories, and conversation. So I built the most literal version of that I
could think of: a way to sit down and have a conversation with the past.
The past, it turns out, has opinions. Mostly about young programmers and
their 400 dependencies.

## Demo

**Live demo (GitHub Pages):** https://l28159363-cloud.github.io/cobol-ghost/

No sign-up, no key, no server. Or download `index.html` and open it with
your internet switched off — it works exactly the same, which is the point.

Things to try:

- Click the sample questions, or ask your own in English: "Who are you?",
  "Are you dead?", "What do you run?", "What about Y2K?", "What do you
  think of Python?", "Tell me a joke", "Show me some code".
- Feed the COBOL-ify machine a sentence and watch it come back as a
  `PROGRAM-ID` with a `WORKING-STORAGE SECTION`.
- Ask it something it does not understand, and enjoy its error messages.
  The ghost is not a search engine and would like you to know it.

## Code

{% link https://github.com/l28159363-cloud/cobol-ghost %}

The whole project is one file — `index.html` — plus a README, a LICENSE
(MIT), and this post draft. No frameworks, no CDNs, no build step. The
repository also contains the full dialogue rule table, so you can read
every line the ghost is capable of saying.

## How I Built It

Let me be honest about what the ghost is, because the honesty is the design.

There are no model weights in this project. No API calls, no keys, no cloud
runtime, no fine-tuning run. The ghost's brain is a hand-written,
deterministic dialogue engine: a keyword-scoring rule table in plain
JavaScript that matches what you type against the things COBOL would
actually brag or complain about, plus a small generator that turns your
sentences into COBOL programs. It was built from scratch on October 29,
2026, inside the challenge window, in a single sitting — one HTML file,
written to be opened and read by anyone.

I know the challenge prompt asks for open-source AI at the core, and I want
to be straight about where this project stands on that: what is "open" here
is everything. Every line of the ghost's mind is open source, MIT-licensed,
and readable in the repository. It runs entirely on your own machine, with
the internet off. It costs nothing. It cannot be revoked, rate-limited, or
discontinued by a provider, because there is no provider.

That last part is not a limitation I worked around — it is the reason the
project works as a piece about ghosts. A séance machine that depends on a
live API is a ghost that dies the day the key expires. COBOL's whole story
is the opposite of that: it survived precisely because it did not depend on
anyone's platform. It ran on mainframes that outlived the companies that
bought them. So I built a ghost the same way: nothing to expire, nothing
to shut down, nothing between you and it except a browser.

The terminal styling is deliberate, too. Green phosphor, a monospace font,
a jobs-processed counter that keeps ticking upward, an ASCII ghost at the
top. The joke lands better when the machine looks like the era the ghost
comes from.

## Why Does Open Innovation Matter?

The challenge asks what open innovation made possible that a closed API
would not. For this project, the answer is simple: it made the ghost
immortal, or at least as immortal as a web page can be.

A closed approach would have meant sending your questions to someone's
model behind someone's key, on someone's server, under someone's terms of
service. That server could go down. The key could expire. The model could
be replaced with a newer one that no longer plays along. Every one of
those is a second death for something that is supposed to be a ghost —
and a strange way to honor a language whose entire legend is refusing to
die.

The open approach flips all of that:

- **It runs on a laptop with no internet.** The demo works offline because
  there is nothing to call. That is not a party trick; it is the whole
  premise. A ghost should not need Wi-Fi.
- **It keeps your words on your own machine.** Nothing you type leaves
  the browser. There is no server to leak it, because there is no server.
- **It costs nothing to run, forever.** No credits, no subscriptions, no
  card on file. The séance is free in the most literal sense.
- **It can be kept alive by anyone.** The code is MIT-licensed and small
  enough to read in one sitting. If I disappear, you can fork it, change
  the ghost's opinions, and summon a different dead language — FORTRAN,
  Ada, Pascal, whatever spirit you miss. The dead stay dead only if
  nobody talks to them.

Open innovation matters here because the theme is about what survives.
Closed systems survive as long as their owners feel like keeping them.
Open systems survive as long as anyone cares. COBOL proved that over
sixty-seven years. This little terminal is just the same idea, shrunk down
to one HTML file.

## The Spirit of It

The moment it landed for me was the first time I asked the ghost the obvious
question: "Are you dead?"

It answered: "DEAD? I MOVE TRILLIONS OF DOLLARS EVERY SINGLE DAY. I AM MORE
ALIVE THAN MOST STARTUPS. THEY CALL ME A GHOST BECAUSE THEY CANNOT SEE ME.
I AM EVERYWHERE."

It is a joke, and it is also true, and that is why it gave me a small chill
in the best way. We spend our careers declaring technologies dead — COBOL,
the mainframe, the terminal itself — and then we go on using them, quietly,
every day, to move money and pay people. The ghost in this machine is not
haunting us. It is doing payroll.

That is what I wanted to build for this week: not a horror prop, but a
remembrance. Día de los Muertos is not about being afraid of the dead; it
is about setting a place for them and keeping the conversation going. So
here is a place, set, for a language born in 1959 that never left. Pull up
a chair. It has been waiting — in ALL CAPS — for sixty-seven years.
