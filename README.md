# Diwakar Mishra

Software engineer. I build complete products — data model, algorithm, interface.

B.Tech CSE-AI at Maharaja Agrasen Institute of Technology, Delhi — CGPA 9.43/10, graduating 2028. Both projects below are built around one question: *why should you believe this?* Starweave won't draw a line between two bands unless someone said it on the record, and links you to where they said it. Arthouse Atlas won't rank one film above another unless the critics' lists agree, and shows you the arithmetic.

`TypeScript` `JavaScript` `React` `Next.js` `Node.js` `Express` `MongoDB` `Tailwind CSS` `Canvas API` `d3` `framer-motion` `Vitest` `GitHub Actions` `C++` `SQL`

---

## Projects

### [Starweave](https://starweaves.vercel.app/) — who influenced whom in indie music, with proof for every line

[![Starweave: Radiohead's musical family, with the bands that shaped them above and the bands they shaped below](https://raw.githubusercontent.com/DiwakarMishra-CODER/starweave/main/docs/screens/clip-family.webp)](https://starweaves.vercel.app/)

A map of 312 artists and 1,024 influence links, all leading back to the Velvet Underground. Streaming apps show you bands that *sound* like the one you love. Starweave shows the bands they actually learned from, and no audio algorithm can find those. Every link is sourced by hand, and every page is a room in the indie world: the map is a night sky, an artist's page is a Tiny Desk set with instruments you can play, and the genres page is a music paper with a pull-out city map.

- **Every link carries its proof.** Each one points to the interview, video or book page that says it, and opens on the exact sentence, highlighted. 772 of the 1,024 are the artist's own words. The sources come from 242 sites and 21 books. The build refuses to ship if the sourcing ledger and the map disagree. 18 recorded *denials* ("we were never influenced by them") are kept too, so a myth can't be added back later.
- **The best-evidenced route, not the shortest.** "Connect two artists" runs Dijkstra, and each hop costs whatever its evidence is worth: the artist's own words cost 0.10, a critic's comparison 0.60. Across 597 random pairs, the fewest-hops route was entirely in the artists' own words 42% of the time. The best-evidenced route was 88% of the time, for about a third of an extra hop.
- **Layout is an algorithm.** The genre family tree fits 52 genres onto 13 roads using heavy-path decomposition and greedy interval colouring. The scenes lightbox is spaced by a longest-path pass, with the frame size picked by binary search. Tests check that every label fits its sign.
- **Fast on canvas.** The force layout runs once at build time, so the map opens settled. Glows are drawn once and stamped, never rebuilt per frame, and animation is measured at 60 fps. Every page shares one layout, so the map never reloads (that cut 5 seconds off the first visit to some pages). The music drives the motion: an audio analyser reads each song against its own loud and quiet range.
- **180 tests in CI**, axe-core accessibility checks, keyboard navigation throughout, and no flashes anywhere (they can trigger photosensitive epilepsy).

`Next.js 16` `React 19` `TypeScript` `d3-force` `Canvas API` `Web Audio API` `Vitest` — [Live](https://starweaves.vercel.app/) · [Source](https://github.com/DiwakarMishra-CODER/starweave)

### [Arthouse Atlas](https://arthouse-atlas.vercel.app/) — 1,120 films, ranked by what critics agree on

[![Arthouse Atlas: the wall of every film's stills dives into today's film](https://raw.githubusercontent.com/DiwakarMishra-CODER/Arthouse-Atlas/main/docs/screens/clip-home.webp)](https://arthouse-atlas.vercel.app/)

A full-stack atlas of arthouse cinema covering 1,120 films, 238 directors, 27 movements and 75 countries, from 1915 to 2025. The order comes from 20 public sources: the Sight and Sound polls, festival juries, year-end lists and more. **For You** recommends films using what 200,000 real viewers loved. Every page is designed as a room of a cinema: a film's page plays its own opening titles, and For You is a camera monitor pulling focus from a film you loved to your pick.

- **A fair ranking from messy sources.** Each of 4,187 citations is weighted by how high the film placed. Similar lists are grouped into capped families, so five year-end lists drawing on the same critics can't count five times. Films earn a bonus for staying power across decades, and young films are judged only by lists they could have been on. The About page walks through the whole calculation for a real film, and a test checks that it reproduces all 1,056 stored scores exactly.
- **A recommender, written from scratch and tested honestly.** It uses EASE (Steck, 2019) trained on 32 million MovieLens ratings. The closed-form matrix solve is written by hand in JavaScript, with no ML library. The test was committed to git *before* it was run, on 11,090 people the model never saw. Each version had to beat the last on that test. The hand-tuned engine put a person's next loved film in the top 10 for 7.4% of them, out of 1,000+ films. The first learned model reached 25.4%, and EASE reached **34.8%**, against 20.9% for just showing the most popular films. Every "why we picked this" is a real head-count.
- **Fast first paint.** All 1,116 films' stills are packed into one sprite sheet, decoded off the main thread with `createImageBitmap`. That took main-thread work on a first visit from 0.5–0.9 s down to under 0.1 s. A film's opening never goes black while it waits on an image.
- **Previews and search for a single-page app.** An edge middleware writes each page's title, image and schema.org data into the HTML, so WhatsApp, LinkedIn and Google see all 1,454 pages properly.
- **Sign-in that can't be borrowed.** A Google token is accepted only once Google confirms it was issued to this site, so a token from another app can't sign its user in here. Unverified emails are refused, since accounts are matched by email. Logins are rate-limited, and errors never leak details. It's all covered by 107 tests, with zero axe-core violations on every page.

`React 19` `Node.js` `Express` `MongoDB` `framer-motion` `d3-geo` `TMDB API` `MovieLens 32M` — [Live](https://arthouse-atlas.vercel.app/) · [Source](https://github.com/DiwakarMishra-CODER/Arthouse-Atlas)

---

## Proof

| | |
|---|---|
| **9.43 / 10** | CGPA · B.Tech CSE-AI |
| **1800+** | LeetCode contest rating · [350+ solved](https://leetcode.com/u/DiwakarCracksIt/) |
| **Semi-Finalist** | Flipkart GRiD 8.0 — national |
| **Neighbourly Choice** | Award for [CareerSaarthi](https://github.com/DiwakarMishra-CODER/CareerSaarthi), a team-built AI career toolkit · [CodeX Hackathon, MAIT](https://drive.google.com/file/d/1twj-CP21e-ugMuo01qvEr7PJ1mL4SFJ1/view?usp=sharing) |

---

## How I think

- **Find it on the page before you claim it.** A search tool once invented a quote outright, so on Starweave a quote counts only after it has been read on its source page. An AI-written wiki that swaps in believable fake influences is banned outright.
- **Write the test down before you run it.** The recommender's evaluation was committed before it ran. When the catalogue grew and every score went down, the baselines' included, I reported the lower number and explained why.
- **Agreement should count; repetition shouldn't.** Five lists that copy each other are one opinion, and the same bio copied across ten sites is one unsourced claim, not ten. Both projects are built so that echoes don't add up.

---

## Let's talk

Graduating 2028, based in Delhi. Open to SDE internships now and new-grad roles after that.

[diwakarmishraemail@gmail.com](mailto:diwakarmishraemail@gmail.com) · [Portfolio](https://diwakar-mishra-portfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/diwakar-mishra-dev) · [LeetCode](https://leetcode.com/u/DiwakarCracksIt/)

Starweave and Arthouse Atlas both came out of the same sleepless night.
