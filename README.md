# The Ghost of COBOL — An Offline Séance Terminal

> A single-page chatbot that channels the spirit of COBOL, a programming language
> pronounced dead for decades that never actually died.
> Built from scratch on October 29, 2026, for the
> **Hacktoberfest DEV Challenge, Week 4: Ghost in the Machine** (October 26–31, 2026).

## Try it

**Live demo (GitHub Pages):** https://l28159363-cloud.github.io/cobol-ghost/

No server, no sign-up, no key. You can also download `index.html` and open it
with the internet switched off — it still works.

## How to play

- **Talk to the ghost.** Type a question in English (or click one of the sample
  questions). The ghost answers in ALL CAPS, as it has since 1959.
- **Ask the classics:** "Who are you?", "Are you dead?", "What do you run?",
  "What about Y2K?", "What do you think of Python?", "Tell me a joke",
  "Show me some code".
- **Try the COBOL-ify machine.** Type any sentence and the ghost turns it into
  a proper COBOL program, complete with `IDENTIFICATION DIVISION`,
  `WORKING-STORAGE SECTION`, and `STOP RUN`.

## Why COBOL?

COBOL was born in 1959, designed by the CODASYL committee with Grace Hopper's
FLOW-MATIC as a major influence, so that programs could read almost like
English sentences. It went on to run the world's banks, ATMs, payroll systems,
insurance claims, and government checks. By one widely cited estimate, around
220 billion lines of COBOL remain in production use, and trillions of dollars
in commerce flow through COBOL systems every day.

People have been predicting COBOL's death for forty years. It never died.
That is exactly what *Ghost in the Machine* means: a spirit from the past
still humming inside the machines we use every day — and during the stretch
from Halloween (October 31) to Día de los Muertos (November 1–2), when the
line between past and present feels thinner, what better way to honor the
past than to sit down and talk to it?

## How it works

The whole project is **one file**: `index.html`. Pure HTML, CSS, and
JavaScript — no frameworks, no CDNs, no build step, no external API calls,
no API keys, no cost.

The ghost's brain is a hand-written, deterministic dialogue engine:
a keyword-scoring rule table that matches what you type against the things
COBOL would actually brag or complain about (banks, ATMs, Y2K, Python,
young programmers, Grace Hopper), plus a small COBOL code generator for the
COBOL-ify machine. Every line the ghost can say is readable in the source.

## Why open matters here

- **It runs with the internet off.** A séance that needs a live API is a
  ghost that dies when the key expires. This one cannot be switched off.
- **Your words never leave your machine.** Nothing is sent anywhere,
  because there is nowhere to send it to.
- **It costs nothing, forever.** No credits, no subscriptions, no cards.
- **It is fully inspectable and forkable.** The ghost's entire mind is
  open source under MIT — read it, remix it, summon your own dead language.

## Project structure

```
cobol-ghost/
├── index.html    # the whole demo: terminal UI + dialogue engine + COBOL-ify
├── README.md     # this file
├── DEV_POST.md   # draft of the DEV challenge submission post
└── LICENSE       # MIT
```

## License

MIT — see [LICENSE](LICENSE).
