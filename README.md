# Signal & Weight

An interactive, click-and-drag primer on machine learning for people who have
never written code — built to hand to complete beginners (including
non-technical professors) and let them learn by breaking things, not by
reading slides.

**[Live demo →](index.html)** (open `index.html` directly in any browser, or
serve the folder with GitHub Pages — see below)

## What's inside

A single self-contained page (`index.html`, no build step, no dependencies
beyond two Google Fonts) with ten exhibits:

| # | Exhibit | What you play with |
|---|---------|---------------------|
| 00 | **Glossary** | 56 flip-cards covering every core ML term, filterable by topic and searchable |
| 01 | **How a Model Learns** | Drag a "model complexity" slider and watch the same 18 points get underfit, then overfit |
| 02 | **Finding the Bottom** | Click to drop a ball on a loss curve, then run gradient descent — including into a local minimum |
| 03 | **Inside a Neuron** | Drag two inputs and drag *directly on the weight lines* of a tiny neural network — including with a keyboard — and step through the arithmetic |
| 04 | **Breaking Language Into Pieces** | Type anything and watch it get tokenized, word-level or subword-level, with live token IDs |
| 05 | **Meaning as Coordinates** | A toy 2-D embedding space of ~48 words — click or drag any word and watch its nearest neighbors update |
| 06 | **Putting It Together** | A Query/Key/Value self-attention demo with positional encoding: tokenize a sentence, click a word to see what it attends to and the blended result it carries forward |
| 07 | **Where the Line Gets Drawn** | Drag a classification threshold and watch the confusion matrix, precision, and recall update live |
| 08 | **Seeing in Patches** | Pick or hand-write a convolution kernel and watch it slide across a pixel grid you can draw on |
| 09 | **Training vs. Prompting** | A toggle contrasting what actually changes on disk when you fine-tune a model versus when you just type instructions to it |

Exhibits 03–05 are the three concepts (neurons, tokenization, embeddings)
that trip up newcomers first — the sidebar nav flags them so you can jump
straight there mid-lecture, and it highlights whichever exhibit is on screen
as you scroll.

Exhibit 06 is a deliberately simplified teaching model of self-attention, not
a real trained transformer — it uses fixed, hand-picked stand-ins for the
Q/K/V projection matrices a real transformer learns. For a full-fidelity,
real-weights walk through an actual GPT-2 model, see the excellent
[Transformer Explainer](https://poloclub.github.io/transformer-explainer/)
(Polo Club / Georgia Tech, in collaboration with IBM), which inspired
Exhibit 06.

## Using this to teach

- Everything runs client-side in the browser — nothing is sent anywhere, no
  account or install needed. Project it, or just send students the link.
- Use the sidebar to jump straight to whichever exhibit answers the question
  that came up in class.
- Every widget resets safely — there's no way to "break" the page, so
  encourage people to drag things to extremes and see what happens.

## Running locally

No build step. Either:

```bash
# just open it
open index.html        # macOS
start index.html        # Windows
```

or serve it (needed for some browsers' stricter font-loading policies):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. In the repo's **Settings → Pages**, set the source to the `main` branch,
   root folder.
3. GitHub will publish it at `https://<username>.github.io/<repo>/` within a
   minute or two.

## License

MIT — see `LICENSE`. Use it, fork it, teach with it.
