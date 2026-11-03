# EnglishBookAi

![Views](https://hits.sh/github.com/RasimAghayev/EnglishBookAi.svg?label=views&color=0e75b6)


## What this is

A complete, standalone English-grammar reference book — **not an application**.
There is no source code, no dependencies, no build step, and nothing to run;
the repository *is* the book. GitHub's own description for it: *"English book
write with AI."*

It targets Azerbaijani-speaking learners from A1 to C2, with bilingual
(English + Azerbaijani) explanations throughout, and covers every English
tense plus the grammar structures around them (modals, conditionals, passive
voice, reported speech, relative clauses, and more).

## Structure

- **49 chapters**, one self-contained Markdown file each, organized into 11
  parts (`00` Foundations → `49` Final Mastery Test). The full map is
  [`00_Table_of_Contents.md`](00_Table_of_Contents.md).
- [`Concept_Index.md`](Concept_Index.md) cross-references every grammar
  concept to where it is introduced, compared against look-alikes, reused in
  later chapters, drilled, summarised, and finally tested.
- Every teaching chapter follows the same structural blueprint — Introduction,
  Why, Real-life situations, Timeline, Formula, Rules, Signal Words, Common
  Mistakes, Comparison, AZ tips, Pronunciation, multi-domain examples,
  Speaking/Writing/Listening/Reading tips, FAQ, Summary — plus a practice
  block (CEFR-leveled examples, vocabulary, idioms, a mini-story with an AZ
  translation, dialogues, and exercises with answer keys). Verified by
  sampling chapters across the book: 03, 09, 24 and 32 each contain 43–62
  `##`-level sections, consistent with the documented blueprint, not just
  described in the TOC.
- Reference appendices: an irregular-verbs list, a signal-words master list,
  a bilingual glossary, consolidated answer keys, a CEFR/IELTS roadmap, and a
  final A1→C2 mastery test.

## Verified claims

- **49/49 chapters complete.** Confirmed against the TOC and `git ls-files`
  (51 tracked `.md` files total: the TOC + 49 chapters + the Concept Index).
- **Link integrity: 0 broken links.** Independently re-checked all 206 inline
  cross-file links and all 49 reference-style link definitions (255 total
  file-links) — every one resolves to a real file in this repo. This matches
  the repo's own final validation pass (commit `cef512e`, which additionally
  claims 591 total inline links and 385 in-page anchors checked; that finer
  in-page-anchor count was not independently re-verified here).
- **No stale chapter-numbering references remain.** The TOC's own
  "Restructure note" still warns that inline `Ch.N` cross-references "may
  still point to old numbers" from an earlier 27-file plan — but that was
  fixed in review commit `c346332` (2026-07-02), and a fresh scan here found
  zero `Ch.N` references outside the valid 1–49 range. The warning note
  itself is now stale documentation describing an already-fixed risk, not a
  live one.
- **Azerbaijani dotted-İ anchor handling.** GitHub's Markdown slugger keeps
  Unicode combining marks, so the Azerbaijani capital İ doesn't slug the way
  a naive anchor would. Two on-page menu links in Chapter 44 were hardened
  with explicit `<a id>` anchors to route around it (commit `cef512e`).
- **Push date is accurate here** — unlike several other repos in this
  portfolio, where GitHub's reported push date belonged to an unmerged
  Dependabot/Renovate branch rather than the default branch. This repo has
  only `master` (no other remote branches, 0 open PRs, 0 open issues), and
  its GitHub `pushedAt` timestamp matches the final commit exactly.

## Authorship, transparently disclosed

This is an AI-co-written book, and it says so in its own git history, not
just its GitHub description: **all 75 commits** in this repository — from
the first `.gitignore` commit through the final link-validation pass — carry
an explicit `Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>`
trailer. That's consistent, disclosed authorship throughout, not a finding to
flag or redact.

## What's intentionally not here

No LICENSE file, no CI workflow, no GitHub Pages, no application code, and no
dependencies — this is a pure-content repository, so none of the usual
software checks (build, test, audit) apply.
