# Diwakar Mishra

Software engineer. I build complete products — data model, algorithm, interface.

I pick problems that need more than a database. B.Tech CSE-AI at Maharaja Agrasen Institute of Technology, Delhi — CGPA 9.43/10, graduating 2028. Every project below comes down to a scoring system: how much a citation is worth, how much a click is worth, how much a good answer is worth. All three show their working rather than asking you to take it on faith.

`React` `Next.js` `TypeScript` `Node.js` `Express` `Supabase` `MongoDB` `Tailwind CSS` `C++` `SQL` `LLM Integration` `Git · CI`

---

## Projects

### [Starweave](https://starweaves.vercel.app/) — 1,053 influence edges across 297 artists

[![Starweave](https://diwakar-mishra-portfolio.vercel.app/projects/starweave.png)](https://starweaves.vercel.app/)

Influence isn't the same as sounding similar — a band can shape another that sounds nothing like it, so no audio algorithm can find these links. Every edge is sourced by hand: 908 of 1,053 cite a named source, 562 the artist's own words. The 145 nobody has said on the record are marked `unsourceable` rather than quietly asserted, and 30 recorded denials are stored separately so a myth an artist has rejected can't be rediscovered later. Asking how two artists connect runs Dijkstra over a cost function where the hop price *is* the citation tier — 0.10 for the artist's own words, 0.85 for unsourced — so the search returns the best-evidenced route, not the shortest one. Weakly-sourced links on the average route drop from 70% to 11% for under one extra hop.

`Next.js` `TypeScript` `d3-force` `Canvas API` — [Live](https://starweaves.vercel.app/) · [Source](https://github.com/DiwakarMishra-CODER/starweave)

### [Arthouse Atlas](https://arthouse-atlas.vercel.app/) — 497 curated films across 12 movements

[![Arthouse Atlas](https://diwakar-mishra-portfolio.vercel.app/projects/arthouse-atlas.png)](https://arthouse-atlas.vercel.app/)

497 films kept from a much longer list, curated across directors, movements, and decades. Every ranking is arithmetic you can read, not a model you have to trust: the Explore feed scores each film on `0.60 × canon + 0.20 × recency + 0.10 × rarity + 0.10 × daily rotation`, and every film returned increments its own show count — so the rarity term keeps doing its job and the canon doesn't win every single visit. Recommendations run the same honesty on top: a taste profile weighted by interaction type (favorites 3x, watched 1.5x, watchlist 1x) scores 200 candidates per request.

`React` `Node.js` `Express` `MongoDB` `TMDB API` — [Live](https://arthouse-atlas.vercel.app/) · [Source](https://github.com/DiwakarMishra-CODER/Arthouse-Atlas)

### [CareerSaarthi](https://careersaarthi.vercel.app/) — 6 AI tools behind one career workflow

[![CareerSaarthi](https://diwakar-mishra-portfolio.vercel.app/projects/careersaarthi.png)](https://careersaarthi.vercel.app/)

Built with a team at my first hackathon. A teacher asked what made our resume analyser unique and we had no answer, so we built the other five tools around it — these exist scattered across the internet behind separate logins, and here they share context. No provider key ever reaches the browser: every OpenRouter and Gemini call is proxied through Express, with a pool of Gemini keys rotated per request and backed off on rate limits instead of hard-failing. The voice coach speaks each question, transcribes live, auto-submits after 2.5 seconds of detected silence, and scores clarity, STAR structure, and keyword density.

`React` `Supabase` `Web Speech API` `GPT-4o-mini` — [Live](https://careersaarthi.vercel.app/) · [Source](https://github.com/DiwakarMishra-CODER/CareerSaarthi)

---

## Proof

| | |
|---|---|
| **9.43 / 10** | CGPA · B.Tech CSE-AI |
| **1800+** | LeetCode contest rating · [350+ solved](https://leetcode.com/u/DiwakarCracksIt/) |
| **Semi-Finalist** | Flipkart GRiD 8.0 — national |
| **Neighbourly Choice** | Award · [CodeX Hackathon, MAIT](https://drive.google.com/file/d/1twj-CP21e-ugMuo01qvEr7PJ1mL4SFJ1/view?usp=sharing) |

---

## How I think

- **Layout is an algorithm.** Starweave's genre map packs 53 timelines into the fewest rows — heavy-path decomposition, greedy interval colouring, no labels colliding.
- **Curate by cutting.** Critics' polls and festival canons don't agree on one list. Arthouse Atlas merges them, then cuts what's too mainstream.
- **Plan for the API failing.** Rate limits, dead APIs, blank screens. A cache absorbs the first; fallbacks cover the rest.

---

## Let's talk

Graduating 2028, based in Delhi. Open to SDE internships now and new-grad roles after that.

[diwakarmishraemail@gmail.com](mailto:diwakarmishraemail@gmail.com) · [Portfolio](https://diwakar-mishra-portfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/diwakar-mishra-dev) · [LeetCode](https://leetcode.com/u/DiwakarCracksIt/)

Starweave and Arthouse Atlas both came out of the same sleepless night.
