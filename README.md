# From Vectors to Transformers

**A 41-day course: everything you need to read an AI research paper.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-c65d21.svg)](LICENSE)

📘 **[Download the book (PDF, 202 pages)](From-Vectors-to-Transformers-final.pdf)**

---

## What this is

Most machine-learning papers are not hard. They are written in a notation
nobody teaches you.

This book takes a working software engineer from "a vector is an array" to
reading *Attention Is All You Need* line by line. Forty-one lessons, each about
a fifteen-minute read, each with a worked example, a self-check with full
answers, and figures drawn specifically for the point being made.

It started as a personal project: one lesson every morning until I could read
the papers I kept seeing referenced and could not follow. This is the result,
cleaned up and made shareable.

## What it is not

- Not a PyTorch tutorial. You will not train a model.
- Not a survey of the field.
- Not a replacement for the papers — it is the thing that makes them readable.

## Who it's for

Software engineers who use AI tools daily and want to understand what is under
them. If you can read a function signature and reason about a data structure,
you have enough background. University calculus helps but is not required —
Lessons 4 and 5 build the derivative and the gradient from nothing.

## Contents

| Stage | Lessons | What you get |
|---|---|---|
| **One — Math Essentials** | 1–10 | Vectors, matrices, dot products, derivatives, gradients, probability, expectation, cross-entropy |
| **Two — Neural Network Fundamentals** | 11–24 | Neurons, activations, layers, loss, gradient descent, backpropagation worked by hand, the training loop, overfitting, embeddings, softmax |
| **Three — The Transformer** | 25–38 | Tokenization, embeddings, attention from first principles, Q/K/V, multi-head, positional encoding, residuals, the full GPT stack — then *Attention Is All You Need*, read in full |
| **Four — How LLMs Work** | 39–41 | Pretraining and next-token prediction, datasets and corpora, scaling laws |

**The turning point is Lesson 30**, where you compute attention weights by hand
on a four-word sentence. After that, attention stops being magic and becomes
arithmetic. Lessons 36 and 37 then read the paper section by section, and it
feels ordinary.

## Companion material

- Andrej Karpathy, *Neural Networks: Zero to Hero* — alongside Stage Two
- Jay Alammar, *The Illustrated Transformer* — alongside Stage Three
- Karpathy, *Let's build GPT* — after Lesson 35

## Repository layout

```
From-Vectors-to-Transformers-final.pdf   the book, with covers
AI-Manual-full-book.md                   merged manuscript
lesson-NN-*.md                           the 41 lessons, one file each
lesson-NN-figN-*.png                     all 82 figures
figstyle.py                              shared matplotlib style
build_book.py                            merges lessons into the manuscript
build_pdf.sh                             renders the manuscript via pandoc + XeLaTeX
add_covers.py                            binds the covers onto the interior
header.tex, titlepage.tex                LaTeX styling and front matter
cover-front.png, cover-back.png          cover artwork
```

## Rebuilding the book

Requires `pandoc`, `xelatex`, and Python with `matplotlib`, `pypdf`, `pillow`
and `reportlab`.

```bash
python3 build_book.py     # merge the 41 lessons into one manuscript
bash    build_pdf.sh      # typeset the interior
python3 add_covers.py     # bind on front and back covers
```

## Corrections

Errors are the thing I most want to hear about. Open an issue with the lesson
number and the sentence, and I will fix it and rebuild. Every hand-worked
number in the book has been recomputed and verified, but the field moves and
mistakes survive review — if you find one, you are doing me a favour.

## Licence

[CC BY-NC-SA 4.0](LICENSE). Share it, translate it, teach from it, build on it
— credit the source, don't sell it, and license derivatives the same way.
Translations are especially welcome.

The papers discussed remain the work of their authors and are described here as
commentary and teaching; none of them is reproduced. All 82 figures are
original, generated from the scripts in this repository.
