# Coding-quiz-1

# BUILD::QUIZ — Auth & Express Fundamentals

A single-file coding quiz app that tests real backend fundamentals — Node.js, Express, bcrypt, and JWT — using questions and code pulled straight from a working auth stack (register/login routes, controllers, and server entry file).

Dark-terminal aesthetic with a build-log style progress bar, gold/cyan accent palette, and instant per-question feedback.

---

## Live Demo

Open `backend-quiz.html` directly in any browser, or deploy to Neocities / Netlify as a static file — no build step required.

---

## Features

- **30 questions total**
  - 10 theory checks (multiple choice) — salt rounds, JWT expiry, status codes, middleware, auth vs. authorization
  - 20 "complete the code" prompts — fill in the missing line in real Express/Node snippets
- **Terminal build-bar** — progress track, live score, phase labels styled like a CI build log
- **Instant feedback** — correct/wrong states with a short explanation after each answer
- **Pass/fail verdict** — 80% threshold, styled as `BUILD PASSED` / `BUILD FAILED`
- **Missed-answer log** — review every incorrect question and its correct answer at the end
- **Zero dependencies** — single HTML file, inline CSS + vanilla JS, no frameworks or build tools

---

## Tech Stack

| Layer      | Choice                              |
|------------|--------------------------------------|
| Structure  | Single-file HTML5                    |
| Styling    | Inline CSS, custom properties        |
| Fonts      | JetBrains Mono (code/data), Space Grotesk (headings) |
| Logic      | Vanilla JavaScript, no libraries      |
| Hosting    | Neocities / Netlify / Render static  |

---

## File Structure

```
backend-quiz.html   → entire app (markup, styles, logic, question data)
README.md            → this file
```

No subdirectories, no build pipeline — matches the flat, mobile-first project structure used across the rest of this portfolio.

---

## Question Bank

Questions are stored as a plain JS array (`questions[]`) inside the file, each with:

```js
{
  phase: 'theory' | 'code',
  q: "question text",
  code: "optional HTML code snippet with a <span class='blank'> marker",
  options: ["A", "B", "C", "D"],
  correct: 0,       // index into options
  explain: "shown after the question is answered"
}
```

To add or edit questions, extend this array — no other code needs to change.

---

## Roadmap

- [ ] Persist scores per user with a small Node/Express + JWT backend (matching the rest of the stack)
- [ ] Leaderboard view
- [ ] Category filter (theory-only / code-only practice mode)
- [ ] Timed mode

---

## License

Personal project — part of the Lona Matshingana developer portfolio.
