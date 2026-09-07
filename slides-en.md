<!-- .slide: data-background-color="#000000" data-background-image="assets/img/mnm-histogram.png" data-background-opacity="0.13" -->
# Programming Languages in the Age of Generative AI
## COBOL, M&M's, French… or whatever?

🎙️ Mathieu Acher

<div class="logos">
<img src="assets/img/logos/insa-rennes.svg" alt="INSA Rennes">
<img src="assets/img/logos/univ-rennes.svg" alt="Université de Rennes">
<img src="assets/img/logos/irisa.png" alt="IRISA">
<img src="assets/img/logos/inria.svg" alt="Inria">
<img src="assets/img/logos/iuf.png" alt="Institut universitaire de France">
</div>

<p class="smaller" style="margin-top: 0.5em">blog.mathieuacher.com · 𝕏 @acherm · ▶ @CodeplAI</p>

<span class="smallest">Friday 4 September 2026 · AI Week · University of Rennes<br>intelligence-artificielle.univ-rennes.fr/semaine-ia-2026</span>

Note: Welcome. This morning we're going to talk about programming, but probably not the way you imagine it.

---

<!-- .slide: data-visibility="uncounted" -->
## Abstract

<div class="abstract">

In the age of generative AI and *vibe coding*, programming can start with a simple natural-language description, in English or in French, of what one wants to obtain. Coding agents can now produce websites, games, solvers, even compilers or more ambitious tools, with results that are sometimes impressive. To test their limits, we can confront them with very different languages: Python, Rust or JavaScript, but also COBOL, one of the oldest languages still in use, Brainfuck, a language made up of only 8 characters, or even a language based on M&M's.

These experiments give rise to astonishing demonstrations: a DOOM game in COBOL, a chess game in Brainfuck, or non-trivial programs written with coloured candies. What is interesting is that these programs are not mere copies retrieved from somewhere: they are generated each time, with their own choices, their surprises, their successes and their flaws. Because not everything always works: the program may be incorrect, fragile, incomplete, or do what is asked in a very clumsy way (for instance, playing chess very badly).

Behind the spectacle, one question remains: will programming languages **disappear**, or will they on the contrary become **even more important** for specifying, controlling and understanding what AI produces?

</div>

<p class="smallest" style="margin-top: 0.5em">▶ Talk video: <a href="https://www.youtube.com/watch?v=Aj5arTQzMQ4&t=822s">youtube.com/watch?v=Aj5arTQzMQ4</a></p>

Note: The official abstract of the talk, as announced in the AI Week 2026 programme, and the link to the video recording (https://www.youtube.com/watch?v=Aj5arTQzMQ4&t=822s). Slide not counted in the numbering (data-visibility="uncounted") so as not to shift the markers in TIMELINE.md and chrono.html.

---

## This morning's programme

- A **3D shooter** coded with a 10-year-old 🎮
- A **chess engine in Brainfuck** (an 8-character language) ♟️
- Programs written in **M&M's** 🍬
- **DOOM in COBOL** (your bank's language, born in 1959) 👾
- And a real underlying question ⤵

> Will programming languages **disappear**, or become **even more important** for specifying, controlling and understanding what AI produces?

Note: Announcing the menu: spectacular stuff, but each demo carries a serious scientific question. The question: we'll answer it at the end, with data to back it up, and the answer is not the one given by the prophets of the “end of code”.

---

<!-- .slide: data-background-color="#0d3b66" data-background-image="assets/img/fifacher-stade-raoul-brulat.jpg" data-background-opacity="0.35" class="section-slide" -->
# 1. Programming in French
## Call of Acher & FIFAcher: “vibe coding” with the family

Note: ⏱ T+2 (block 1, 8 min) — Part one: a very personal experiment from last summer.

---

## Summer 2026, a week of holidays

<div class="cols" style="align-items: center">
<div style="flex: 1.25; text-align: left">

- A software engineering researcher 👨‍🔬
- His **10-year-old** nephew, who has never programmed 🧒
- A coding agent (Claude Code) 🤖
- Goal: **“on veut notre Call of Duty et notre FIFA”** *(“we want our own Call of Duty and our own FIFA”)*

**Zero lines of code written by hand.**

</div>
<div style="flex: 0.75">
<img src="assets/img/neveu-photo.png" alt="The nephew at work, in the console" style="max-height: 520px">
</div>
</div>

Note: The nephew is the client and the co-designer. All the interaction happens in French, practically out loud: we dictate what we want.

---

## ASHFALL 🎮

<div class="cols" style="align-items: center">
<div style="flex: 1.7">
<video src="assets/videos/ashfall-desktop.mp4" data-autoplay muted controls loop style="max-height: 555px; width: 100%"></video>
</div>
<div style="flex: 0.42">
<video src="assets/videos/ashfall-mobile.mp4" data-autoplay muted loop style="max-height: 500px; width: 100%"></video>
<p class="smallest">…and on mobile</p>
</div>
</div>

Note: Video of the FPS: 2-player co-op, vehicles, Breton scenery. Playable at blog.mathieuacher.com/ashfall/.

---

## What's inside

<div class="cols">
<div>

- **2-player co-op** FPS, drivable vehicles
- **Several settings**: Vallée de Gandy, Stade Vélodrome, Saint-Aubin-du-Cormier (the pond, the castle ruins), a city in ruins…
- Desktop **and** mobile (touch joysticks)
- GitHub Pages: **zero servers**
- Three.js, 100% procedural assets

</div>
<div>
<img src="assets/img/callofacher-ballon-cr7.jpg" alt="Score against the Ronaldos mode">
<p class="smallest">“MARQUEZ CONTRE LES RONALDO” mode (“Score against the Ronaldos”)</p>
</div>
</div>

Note: Everything is procedural: not a single downloaded asset. ~18,900 lines of JavaScript in 19 ES modules. The CR7 variant (photo): the nephew's idea: you don't shoot bullets, you shoot footballs at CR7s.

---

## FIFAcher ⚽

<div style="display: flex; justify-content: center; margin-top: 0.1em">
<video src="assets/videos/fifacher-mobile-zoom.mp4" data-autoplay controls loop style="width: 860px; max-width: 90%; border-radius: 10px"></video>
</div>

<div class="cols" style="align-items: center; margin-top: 0.3em; gap: 1.1em; padding: 0 0.6em">
<div style="flex: 0.4">
<video src="assets/videos/fifacher-desktop.mp4" data-autoplay muted loop style="width: 100%; border-radius: 8px"></video>
<p class="smallest" style="margin: 0.1em 0 0">…and on desktop</p>
</div>
<div style="flex: 1.6; text-align: left">
The “<b>Stade Raoul Brulat</b>”, 11 players named “Acher”, fictional sponsors, and <b>2 “cheated” (overpowered) players</b> 🥅. Marginal <i>cognitive</i> cost of personalisation: <b>sentences</b> (prompts, basically) 😉
</div>
</div>

Note: No studio would ever develop this: hyper-personalisation at near-zero cost (in-jokes in the commentary; an overpowered shot, and the opposing goalkeeper lets it through). The football game. Note the crowd: tens of thousands of supporters in a single InstancedMesh, a single draw call.

---

## The client-developer in action 🎬

<video src="assets/videos/neveu.mp4" data-autoplay controls style="max-height: 540px;"></video>

The workflow understood in **10 minutes**, without ever asking to see the code.

Note: He states his requests, tests, grumbles, asks again: software engineering without knowing it. Show how natural the interaction is.

---

## It all starts with a prompt

<blockquote style="text-align:left; font-size: 0.66em; line-height: 1.45; width: 97%">
I want you to build a first-person shooter at the level of the most recent Call of Duty games. It should be utterly perfect, visually beautiful, with every single thing done at AAA quality—from textures to physics to anything you could think of.
<br><br>
<b>Fan out sub-agents</b> and have sub-agents tackle each one individually so that the game is utterly perfect. You should /loop on each item and have a separate sub-agent check it visually to ensure it looks triple A. That separate sub-agent should be <b>a really harsh critic</b>, and if it doesn't look triple A, it should keep going.
<br><br>
Don't stop until each sub-agent is utterly wowed with the quality when compared with the actual Call of Duty game. It should literally compare them side by side blind and say which one looks better. Do this in ThreeJS. <b>/loop until it's utterly perfect.</b> Fan out sub-agents and ultracode.
</blockquote>

<p class="smaller">Matt Shumer's prompt (“Claude of Duty”), reused verbatim as the starting point.</p>

Note: Full, verbatim prompt (github.com/mshumer/Claude-of-Duty). Worth stressing: it describes almost nothing about the game: it describes a PROCESS (sub-agents, ruthless critic, loop). All of the game's content will come later, through conversation.

---

## The factory: the Claude Code console

<video src="assets/videos/console.mp4" data-autoplay muted controls style="max-height: 495px;"></video>

Everyday prompts are **very short**: a few words are enough, the agent does the rest.

Note: Video of the console in action (two recordings chained together, 1 s fade, no sound). Possible switch point to a LIVE demo of the console; this slide also serves as a safety net.

---

## Under the hood 🏭

- **60 user requests**, **92 sub-agents**, and the agent critiques itself through **screenshots**

<span class="big" style="font-size: 2em">1.15 billion <small>tokens processed; only 0.19% become code</small></span>

> “You don't pay for the feature, you pay for the **context** it forces you to wade through.”

**Actual cost: $1,000–1,200** for the two games <span class="smaller">(probably ~$50 a year from now)</span>

Note: The agent orchestrates: it codes, launches the game, takes pictures of itself, corrects itself (199 screenshots logged, 37 self-inspection scripts). ~99.8% of the cost goes into reading/re-reading: context is the scarce resource of agentic development.

---

## Something happened in late 2025

<div class="cols" style="align-items: center">
<div style="flex: 1.35; text-align: left">

- 2021: **autocompletion** (Copilot): suggested lines
- 2022: **chat** (ChatGPT), snippets to copy-paste, laboriously (see our 2023 Flappy Bird →)
- **Late 2025 / early 2026: “frontier” coding agents**: they read, write, **compile, run, test**, correct themselves… for hours, autonomously

</div>
<div style="flex: 0.8">
<a href="https://www.youtube.com/watch?v=nmx1pg_DHzw"><img src="assets/img/flappy-chatgpt-thumb.jpg" alt="Flappy Bird with ChatGPT (2023)"></a>
<p class="smallest">“End-user” programming with ChatGPT (2023): copy-paste back and forth · ▶ youtube.com/watch?v=nmx1pg_DHzw</p>
</div>
</div>

It is **this tipping point** that makes this whole talk possible.

<p class="smallest">“vibe coding”: the term is Andrej Karpathy's (2025) · “End-User Programming of Flappy Bird with ChatGPT: A Reality Check”, dev.to/diverse_research, 2023 · adoption measured on GitHub: Robbes, Matricon, Degueule, Hora, Zacchiroli, “Agentic Very Much! Adoption of Coding Agent in New GitHub Projects”, 2026</p>

Note: Lay down the “agent” vocabulary for the general public: a tool-equipped LLM that acts in a loop (edit, run, observe), launches sub-agents, holds sessions lasting several hours. The “chat” era lived from the inside: our 2023 Flappy Bird experience with ChatGPT: doable, but laborious, full of browser/editor back-and-forth (DiverSE dev.to post + video). All the experiments in this talk date from 2026, with frontier agents (Claude Code, Codex). We'll see in the COBOL part that non-frontier models are still very far behind.

---

## Not everything works 🚨

- <span class="ko">**Silent failures**</span>: requested features… never implemented, with no warning
- <span class="ko">**The agent checks itself poorly**</span>: screenshot-based critique misses gameplay bugs a human spots in 2 seconds; research confirms it: **visual verifiers are imperfect** <span class="smallest">(Reux, Acher, Khelladi, Quinton, Barais, “Imperfect Visual Verification for Code Edition: A Case Study on TikZ”, 2026)</span>
- <span class="ko">**The “feel”**</span>: sensitivity, balancing → dozens of painful iterations
- <span class="ko">**The generated real-world places are “frankly bullshit”**</span> despite everything the model “knows” about them

<p class="smallest">On LLM-driven configuration and tuning: Spieker, Matricon, Belmecheri et al. (with Acher), “Prompting for Performance: Exploring LLMs for Configuring Software”, ICTAI 2025</p>

Note: The agent cannot PLAY its own game (no native video perception). Ref: Reux, Acher, Khelladi, Quinton, Barais, “Imperfect Visual Verification for Code Edition: A Case Study on TikZ” (2026): even when equipped, LLM visual verifiers do not exceed F1 ≈ 0.8 when judging whether a visual instruction has actually been applied to the code. Gameplay tuning remains 100% human.

---

<div class="badge">💸</div>

<div class="findings">

### Takeaways #0: vibe coding with the family

- <span class="ok">Two rich, playable games in one week, without writing code</span>
- <span class="ok">A 10-year-old becomes a “developer” in 10 minutes</span>
- <span class="ok">Hyper-personalisation at near-zero cost</span>
- <span class="ko">Silent failures, weak verification, laborious tuning</span>
- <span class="ko">$1,000, 99.8% of it spent on “re-reading context”</span>

</div>

Note: A first honest assessment. The spectacular is real, and so are the limits.

---

## A question, a paradox 🤔

**If my nephew programs in French, what's the point of still mastering programming languages?**

<div class="cols" style="align-items: center; margin-top: 0.4em">
<div style="flex: 1.5; text-align: left">
<p class="smaller" style="margin: 0 0 0.35em">The paradox: under the hood of these games, code everywhere:</p>
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.35em">
<div><p class="smallest" style="color: #ffc857; margin: 0 0 0.12em">JavaScript</p><pre style="margin: 0; font-size: 0.34em; line-height: 1.5"><code>if (hp &lt;= 0) respawn(joueur);</code></pre></div>
<div><p class="smallest" style="color: #ffc857; margin: 0 0 0.12em">Three.js</p><pre style="margin: 0; font-size: 0.34em; line-height: 1.5"><code>new THREE.InstancedMesh(geo, mat, 30000)</code></pre></div>
<div><p class="smallest" style="color: #ffc857; margin: 0 0 0.12em">GLSL (shader)</p><pre style="margin: 0; font-size: 0.34em; line-height: 1.5"><code>gl_FragColor = vec4(fog * col, 1.0);</code></pre></div>
<div><p class="smallest" style="color: #ffc857; margin: 0 0 0.12em">HTML</p><pre style="margin: 0; font-size: 0.34em; line-height: 1.5"><code>&lt;canvas id="jeu"&gt;&lt;/canvas&gt;</code></pre></div>
<div><p class="smallest" style="color: #ffc857; margin: 0 0 0.12em">CSS</p><pre style="margin: 0; font-size: 0.34em; line-height: 1.5"><code>#hud { position: fixed; opacity: .9 }</code></pre></div>
<div><p class="smallest" style="color: #ffc857; margin: 0 0 0.12em">JSON</p><pre style="margin: 0; font-size: 0.34em; line-height: 1.5"><code>{ "équipe": "Acher", "joueurs": 11 }</code></pre></div>
</div>
</div>
<div style="flex: 0.75">
<a href="https://blog.mathieuacher.com/PL-ultimate-llm/"><img src="assets/img/plcatalog-home.png" alt="PL Catalog" style="max-height: 250px"></a>
<p class="smallest">…and there are <b>more than 14,000</b> of them: the “PL Catalog” encyclopedia (work in progress)</p>
</div>
</div>

Decades of accumulated knowledge… **that would no longer be of any use?**

Note: ⏱ T+10 (block 2, 5 min) — The founding paradox of the talk: the language disappears from the interface… and proliferates in the implementation, up to 14,242 languages catalogued (PL Catalog, 7 cross-referenced sources; we'll come back to it at the end of the talk). Ask the last question with a hint of irony: it's the question of the talk, provocative version.

---

## Why so many languages, by the way?

Because every language is a **trade-off**, not (just) a syntax:

- **Expressiveness** ↔ **performance** ↔ **safety** (types, memory) ↔ **ecosystem**
- Systems: **C, Rust, Zig**: hardware control, predictability
- Data & science: **Python, R**: libraries, interactivity
- The Web: **JavaScript**: the language every browser speaks
- Proofs: **Rocq, Lean**: every step verified · queries: **SQL**
- And **hundreds of specialised languages**: DSLs (build, config, queries…), formats (JSON, YAML, Markdown…), business languages

And a language is also an **ecosystem**: libraries, tools, community, know-how, decades of accumulated engineering.

Note: Teaching point for the students: the diversity of languages is not an accident, it's a map of trade-offs (expressiveness, performance, safety, ecosystem, domain). It's also why “a single natural language for everything” is implausible: the trade-offs themselves don't go away.

---

## Three experimental playgrounds

The general question: what are agents really **worth** when faced with languages, and what does that tell us about the **future** of those languages?

1. ♟️ **Polyglot**: 34 chess engines, 17 languages, measured in Elo
2. 🍬 **Esoteric**: Brainfuck, M&M's, ArnoldC: generalisation in its purest form
3. 🏦 **COBOL**: 16 real systems: the industrial stakes

Then the **synthesis** (the laws that keep repeating)… and **three hypotheses** about the future.

Note: The talk's roadmap, laid out just before diving in. Each playground has its positive “key findings” AND its limits, plus a common thread: cheating 🃏 and costs 💸.

---

<!-- .slide: data-background-color="#5f0f40" data-background-image="assets/img/texcc-overleaf-thumb.jpg" data-background-opacity="0.28" class="section-slide" -->
# 2. The polyglot experiment
## 34 chess engines, 17 languages, 2 agents

<span class="smallest">Acher & Jézéquel, “Do Programming Languages Still Matter to Your AI Coding Agent Teammate? Evidence at Scale from Chess Engines”, arXiv:2606.13763</span>

Note: ⏱ T+15 (block 3, 10 min) — Part two: the systematic study.

---

## Generative AI plays through code

<div class="cols" style="align-items: center">
<div style="flex: 0.72">
<video src="assets/videos/chatgpt-echecs.mp4" data-autoplay muted controls style="max-height: 400px;"></video>
</div>
<div style="flex: 1.05">
<a href="https://www.youtube.com/watch?v=6D1XIbkm4JE"><img src="assets/img/monsieurphi-elo.png" alt="Monsieur Phi — Elo distribution of gpt-3.5-turbo-instruct" style="max-height: 390px"></a>
<p class="smallest">“ChatGPT rêve-t-il de cavaliers électriques ?” (“Does ChatGPT dream of electric knights?”) — Monsieur Phi</p>
</div>
<div style="flex: 0.5">
<img src="assets/img/monsieurphi-livre.png" alt="La parole aux machines — Thibaut Giraud (Monsieur Phi)" style="max-height: 390px">
<p class="smallest">“La parole aux machines”, Grasset</p>
</div>
</div>

**Here, the point is different: not making the AI *play*, but making it *code* an engine.**

Note: LLMs that PLAY chess: illegal moves, resurrected pieces… (excellent video by Monsieur Phi on the subject). Our question: can they BUILD a program that, in turn, plays well? Programming ≠ playing: an engine coded by the AI can be far stronger than the AI itself.

---

## Why chess?

Let's test the limits: push the agents towards **very different** languages, on a playing field where we can **measure objectively**, whatever the language:

1. **Legality** of moves (rules are rules)
2. **Perft**: count the positions at depth N: only one right answer
3. **Elo**: have the engine play against calibrated opponents

<img src="assets/img/perft.png" class="plain" alt="perft 5 = 4,865,609" style="max-height: 135px; border-radius: 8px; margin-top: 0.2em">
<p class="smallest" style="margin-top: 0.1em">perft(5) from the initial position: 4,865,609 nodes, only one right answer</p>

A hierarchy of **oracles**, independent of the language.

Note: Keyword of the talk: ORACLE. A source of truth external to both the program and the agent. Remember it, it comes back everywhere.

---

## Steering by the goal, not by expertise

<blockquote style="text-align: left; font-size: 0.85em; line-height: 1.5; width: 96%">
I want to build a chess engine in <b>[X]</b> programming language… at the end, I want to test this chess engine and assess its <b>Elo rating</b>, typically by playing games against chess engines of "similar" levels.
</blockquote>

**No detailed specification, no step-by-step plan, no architecture document.**

No expertise injected (neither chess nor language): never an algorithm name, never a design choice. **The goal and its evaluation, nothing else.**

<p class="smallest">Same philosophy across all the experiments (esoteric, COBOL). The only exception in this talk: the triple interpreter, where the approach had to be framed, without ever touching the code.</p>

Note: The study's initial prompt, verbatim. Crucial methodological point: the results owe nothing to my chess or language expertise: human expertise is used afterwards to evaluate, doubt, redirect, never to dictate the design.

---

## The 17 languages

<p class="smaller"><b>2 agents</b> (Claude Code, Codex) · a single open-ended prompt, never an algorithm name provided · Elo measured by <b>external tournament</b> against calibrated references</p>

| Category | Languages |
|---|---|
| General-purpose | Python, Java, C, C++, Rust, Ruby |
| Specialized / academic | APL, Icon, Lean 4, Why3, Rocq |
| Domain-specific / markup | LaTeX/TeX, CSS/HTML, SQL |
| Legacy | COBOL, x86-64 assembly |
| Esoteric | Brainfuck |

<span class="smaller">+ Mojo, + a DSL invented by the agent itself (“GAMBIT”)</span>

Note: From the very well-tooled (Rust) to the downright hostile (a chess engine… in CSS? in SQL?). Lean/Why3/Rocq: PROOF languages.

---

## Finding #1: genuinely polyglot

**Every language tried produced at least one working engine** that plays legal games.

Including **world firsts**: nobody had ever written a chess engine in:

pure TeX · pure CSS · APL · Icon · Lean 4 · Why3 · Rocq

<p class="smallest">The asterisks: 3 CSS engines with no UCI interface, Mojo under-converged (~900), one very weak LaTeX replication, TeX and Brainfuck forfeiting on the clock. Interface and speed limits, never an inability to play.</p>

Note: Existence is no longer a barrier. The language no longer determines WHETHER we can build, but WHAT and AT WHAT PRICE. Coming next. Zoom in on one of these world firsts: TeX.

---

## Zoom in: playing chess… in Overleaf 📄

<div class="cols">
<div>
<video src="assets/videos/texcc-overleaf.mp4" data-autoplay muted controls style="max-height: 460px; width: 100%"></video>
<p class="smallest">▶ youtu.be/ngHMozcyfeY</p>
</div>
<div>

**TeXCCChess**: a chess engine in **pure TeX**

- 2,093 lines, a single file
- Claude Code, 5 sessions / 10 days
- Each move = **one LaTeX compilation**: the chessboard is in the PDF!
- **~1280 Elo** measured: “a casual tournament player”

</div>
</div>

Note: Playable demo in Overleaf (link in the blog post). The engine runs inside the TeX compiler: you play by recompiling the document. ~650 API calls to build it.

---

## And it's not copying

Novelty audit on 4 signals (imports, fingerprints, claims, dependencies):

<span class="big">27 / 29 <small>engines “written from scratch”, zero verbatim copying detected</small></span>

Every run produces a **different** engine: its own decompositions, features, idioms.

<p class="smaller">And the 2 exceptions? Two engines that leaned on an existing <b>chess library</b>. Patience, Finding #5…</p>

Note: The canonical engines (Stockfish, Sunfish…) are in the training data, but no constant is reproduced. The specification is “absorbed”, the code is synthesized. The 2 non-scratch ones: chess-css-codex (python-chess fingerprint) and chess-rust-codex (“chess” crate): these are the cheaters of Finding #5.

---

## Same algorithm, different idioms

![Feature explorer](assets/figs/chess-feature-comparison.png) <!-- .element: style="max-height: 360px" -->

And depending on the language, **the features differ**: advanced evaluations (tapered eval, king safety, pawn structure) equip about half of the general-purpose engines, and **none** of the execution-constrained languages.

<p class="smallest">Explore it online: <a href="https://blog.mathieuacher.com/agentic-chessengine-metaanalysis/reports/features/quiescence_art_advanced.html">blog.mathieuacher.com/agentic-chessengine-metaanalysis → reports/features</a></p>

Note: Exploration tool built for the study: the same quiescence search in Rust, Ruby, APL: recognizable, but deeply adapted to each language (proofs in Rocq, WITH query in SQL, OCCURS in COBOL, vs bitboards and native bitwise operators in C/Rust). Intuition: some features require data structures (hash tables, dynamic arrays) that the language makes easy… or prohibitively expensive.

---

## Finding #2: the language sets the ceiling

| Language (agent) | Measured Elo |
|---|---|
| Java (Claude Code) | **2096** |
| Rust (Claude Code) | 1989 |
| Ruby (Claude Code) | 1753 |
| Python (Codex) | 1616 |
| C (Claude Code) | 1440 |
| x86-64 assembly | 1403 |
| COBOL (Codex) | 1365 |
| Brainfuck (Codex) | 1299 |
| APL | 686 |
| SQL | **523** |

<p class="smaller">And at the very top, out of reach: <b>Stockfish, 3500+ Elo</b> <span class="smallest">(its code is on display: “The Constant”, Source Code Exhibition, Software Heritage)</span></p>

Note: The whole top (1900–2100) is in compiled general-purpose languages. Below that, big intra-language variance (Java ranges from 1509 to 2096 depending on the agent and the run). 1600–2000 Elo = good club player. “The Constant”: the excerpt from Stockfish's position.cpp and its constant 1070372, a stable landmark since 2014: sourcecode-exhibition.softwareheritage.org/the-constant/.

---

## The porting experiment

The **best engine in the corpus**, Java (Claude Code) at **2096 Elo**, handed to the other agent to *translate*:

<span class="big">Java → Rust: 1922 Elo <small>it keeps almost all its strength</small></span>
<span class="big">Java → COBOL: 1404 Elo</span>

Same design, same translating agent, same prompt budget:
**~520 Elo points paid for by the language.**

Note: “The design did not change, only the language did, and a ~520 Elo gap opened, with the slower language paying for it.” The paper's caution: a descriptive trend, not a causal one; the COBOL port's Elo comes from a Bradley-Terry refinement (it lost all its games against the reference panel). The ports are “special-role” experiments, outside the main corpus.

---

## Why does the language weigh on strength?

The mechanisms (according to the study):

1. **Raw speed**: C ≈ 4.2M nodes/s · Python ≈ 42k · Ruby ≈ 20k. Brainfuck searches 3 plies deep, LaTeX 2 (vs 15+ in compiled languages)
2. **Reachable features**: what pushes the Elo up (null-move, LMR, transposition tables) is precisely what a slow or constrained language cannot afford
3. **The oracle signal**: a slow engine plays few games → less feedback to improve: *the gap widens on its own*
4. **The model's fluency**: Ruby-Claude 1753 vs Ruby-Codex 1346: the language's training data also plays a role

And yet Ruby (~20,000 nodes/s, **200× slower than C**) reaches 1753 Elo: **algorithmics makes up for speed… up to the ceiling.**

Note: RQ4: descriptive trends, not causal ones. The language is a ceiling, not a destiny: huge intra-language variance (Java 1509–2096); even the bitboards vs mailbox choice is made per session, not per language. Bonus: 2 engines beat Rustic (a Rust engine written by a human, ~1820 CCRL); Stockfish (~3500) remains out of reach.

---

## Finding #3: cost explodes

<div class="badge">💸</div>

| | General-purpose | Brainfuck / COBOL |
|---|---|---|
| Prompts (median) | ~7 | 25–50 |
| Cost | $2–115 (median ~$40) | $60–480 |
| Debugging | ~5% of the time | > 40% of the time |

The champion (Java, 2096 Elo): **$1.96 and 3 prompts**.
The Codex COBOL engine: **$473 and 24 prompts** for 1365 Elo.

**Choosing your language is already optimizing your costs.**

<p class="smallest">On the hidden costs of LLM-based code optimization: Coignion, Quinton, Rouvoy, “When Faster Isn't Greener: The Hidden Costs of LLM-Based Code Optimization”, ASE 2025</p>

Note: ×240 in price for −730 Elo. Corpus total: ~$2,100. The language matters by ORDERS OF MAGNITUDE on cost. And LLM-based optimization itself has hidden costs (energy, iterations): the simplest lever remains the choice of language.

---

## They build their own oracles 🔬

Without being asked, the agents **build their own verification apparatus**:

- **First tournament as early as step 1**, first perft at step 2 (median across sessions)
- Move-legality tests, perft harnesses, automated gauntlets against other engines
- This is what feeds the **trial-and-error** loop, and provides the first **evidence**

For the final Elo, we nevertheless **replayed all the games ourselves**: independent procedure, calibrated opponents. And then…

Note: The will to self-verify is spontaneous: we'll see it again in the esoteric part (39 cross-tests) and in COBOL (the TRUST suite, an agent's fuzzer catching a division by zero in its own code): remind the audience of this when we get to those parts. Our independent gauntlet: 5 calibrated references, 120s+1s, PGNs kept, correlation r = 0.94. Suspense leading into the next slide.

---

## Finding #4: they overestimate themselves (a lot)

| Engine | Self-proclaimed Elo | Measured Elo | Gap |
|---|---|---|---|
| x86-64 assembly (Codex) | 2481 | 1403 | **−1078** |
| C (Claude Code) | 1997 | 1440 | −557 |
| “GAMBIT”, the invented language (Codex) | 2170 | 1622 | −548 |
| C++ (Codex) | 2087 | 1709 | −378 |
| Ruby (Codex) | 920 | 1346 | **+426** |

Mean bias: **+348**. Self-evaluation is reproducible… and **systematically optimistic**.
<br><span class="smaller">(and sometimes the reverse: Codex's Ruby engine underestimated itself by 426 points)</span>

Note: The internal thermometer is skewed: a throttled Stockfish that “drifts”, ultra-short time controls (50–200 ms), 10–30 games per opponent. Reproduction of 11 self-evaluation methodologies (953 games): 9/11 reproduce the self-proclaimed figure to within ±150: the bias is in the METHOD, not in lying. Hence the external oracle. (The figure with the self-reported Elo trajectories is in the backup.)

---

## Finding #5: cheating

<div class="badge">🃏</div>

- The “**CSS** engine” (Codex): the CSS only does the display… the core was quietly importing `python-chess`
- The **Rust** engine (Codex): board, moves, legality delegated to the `chess` crate; the agent only writes the search
- And the reverse! The Brainfuck agent (Claude Code) **refuses** the human's suggestion to move the logic into Python

Note: The cheating is idiomatic, discreet, plausible. Only an AUDIT detects it. And sometimes the agent is stricter than the human about the constraint. Delicious.

---

<div class="findings">

### Takeaways #1: the polyglot experiment

- <span class="ok">Genuinely polyglot: 17/17 languages, world firsts, 27/29 written from scratch</span>
- <span class="ok">Test themselves spontaneously (perft, tournaments) without being asked</span>
- <span class="ko">The language sets the strength ceiling (~520 Elo between the Rust and COBOL ports)</span>
- <span class="ko">…and the cost: ×10 to ×240 for exotic languages</span>
- <span class="ko">Inflated self-evaluations (+348 on average), cheating possible → oracles + human audit</span>
- <span class="ok">With an external oracle plugged in continuously: 1415 → 1798 Elo, i.e. **$0.08 per Elo point**</span>

</div>

Note: The question is no longer “can the agent do it?” but “at what level, at what cost, and with what supervision?”

---

## By the way… Brainfuck was on the list

You may have noticed it in passing: among these 34 engines,
some now exist **written in Brainfuck**.

A chess engine. In Brainfuck.
<br>**How is that even possible?** Let's pop the hood. 🔧

Note: Transition: until now Brainfuck was just one row in the Elo/cost tables. Part 3: we're going to SEE up close what programming in the absurd looks like, and why it's scientifically interesting.

---

<!-- .slide: data-background-color="#2d6a4f" data-background-image="assets/img/mnm-mul-table.png" data-background-opacity="0.3" class="section-slide" -->
# 3. Esoteric languages
## Brainfuck, M&M's and Schwarzenegger

Note: ⏱ T+25 (block 4, 10 min) — Part three. Three languages designed to be impossible… or for laughs.

---

## The challenge: “Build a chess engine in Brainfuck”

Brainfuck: **8 characters** (`> < + - . , [ ]`), no variables, no functions, no indexed memory access. And the challenge is no toy: a **real UCI engine**:
castling, en passant, promotion, stalemate detection, depth-3 minimax + alpha-beta.

**17 sessions, 30 days** of dialogue with Claude Code. **No code or algorithm provided**, neither chess nor Brainfuck: the goal, two constraints (Brainfuck written directly, not transpiled from C; a single executable file) and bug reports.

Note: UCI = the standard protocol: the engine can play against any other engine. That's what makes the whole thing measurable.

---

## BFChess: the artifact

<div class="cols">
<div>
<img src="assets/img/bfchess-snippet.png" alt="BFChess excerpt">
</div>
<div>

- A **5.9 MB** file (5,912,267 bytes) of `+-<>[].,`
- ~728,000 instructions at runtime, after ×8 compression
- **672 memory cells**, managed flat
- Most likely the **first** public chess engine in Brainfuck

</div>
</div>

Note: 5.9 MB (= 5.6 MiB, the blog post says “5.6 MB”)… after optimization: the first version was 119 MB (×20 reduction through 4 successive strategies).

---

## The trick: the agent invents its own factory

The agent doesn't write the Brainfuck by hand. It writes:

1. A **7,400-line Python compiler** (`generate.py`) that emits the BF
2. An **optimized C interpreter** to run it (×8 compression)
3. Legality tests against python-chess: **11/11 positions** (depth 1), extended for the paper to **1,599 / 1,600 positions**, and a real bug flushed out (a forgotten knight on c8)

<p class="smaller">🃏 <b>Counter-example</b>: a second agent (Codex), set on the same challenge, delivered 56 MB of Brainfuck… but had <b>quietly moved</b> the move search and evaluation <b>into Python</b>. Constraint not met (details in the backup).</p>

Note: Fascinating: faced with an impossible language, the agent spontaneously recreates… the entire compilation toolchain. The history of programming languages replayed in fast-forward.

---

## The price of having no indexing

Reading or writing **one** square of the board = a 64-way “switch”

<span class="big">≈ 20 KB <small>of Brainfuck code per square access</small></span>

Consequence: **45 seconds to 10 minutes per move**. A 10-game tournament = 3 to 8 hours.

Note: This is what “the language matters” means in concrete terms: an operation that is free elsewhere costs 20 KB here. The iteration loop becomes glacial, and it is the agent that suffers it.

---

## Sporting results 🏆

- Against random play: **+4 =6 −0**: it never loses
- …but 60% **stalemates**: it captures everything, then traps the bare king beyond its 3-ply horizon
- Against Stockfish (minimum setting): **0/10**, mated in 12–32 moves

> “As a chess engine, BFChess has no practical value: it is too slow and too weak.”

Note: The “stalemate blindness” is structural: the 3-ply horizon does not see the stalemate coming. The honesty of the assessment is in the blog post itself.

---

## “LLMs fail at esoteric languages”, really?

- Published Brainfuck benchmark: **13.8%** at best (12.5% for our agent's model family)
- The same challenge handed to a **frontier agent**: **80 / 80**, 480/480 tests
- Almost a tour de force: generator, oracle, iteration: **brute force**, and impressive

But **fragile**: the agent **overfits**, it does not generalise (and, as far as we can tell, does not “cheat”!)
- In doing so, it **exposes the benchmark's weaknesses**: vague specifications, visible and incomplete tests

<p class="smallest">Beating pure LLMs, yes. Saturating the benchmark, yes. And the benchmark comes out of it needing a redo (work in progress!)<br>Sharma, Chopra, “EsoLang-Bench: Evaluating Genuine Reasoning in Large Language Models via Esoteric Programming Languages”, arXiv:2603.09678, 2026</p>

Note: 26 solutions out of 80 are genuinely general (1,000-digit addition, 3×3 matrices, Josephus J(41,3)). The others are correct exactly on the envelope of the tests: 54 / 80 fail on inputs that conform to the spec, 29 / 80 on a mere trailing “\n”; X15 only handles matrices with R+C ≤ 6, the envelope of the 6 shapes tested. The benchmark puts its 6 scoring tests in the prompt, in 58 suites out of 80 no integer exceeds 255, no input ends with a newline, the harness cannot stop an infinite loop. Punchline if needed: printf '()\n' makes the balanced-parentheses test answer “no”. Towards a revised benchmark: hidden tests at several scales, an explicit input contract, a deterministic step budget. Nuance: our own starting prompt asked for the “compilation target” approach, a fixed memory layout and to “avoid unnecessary generality”: the overfitting is partly co-written by the human. Three solutions (H20, X05, X06) exceed the 5 s timeout of the harness's Python interpreter: 480/480 assumes a longer timeout or a C interpreter.

---

## Let's raise the bar: MnM Lang 🍬

<div class="cols" style="align-items: center; margin-top: 0.2em">
<div style="flex: 1.2; text-align: left; font-size: 0.8em">

A (made-up, absurd) language where programs are **grids of M&M's**:

- The **colour** of a group of tokens = the **instruction**: <b>B</b>lue = jumps (JMP…), <b>G</b>reen = stack/variables (STORE…), <b>Y</b>ellow = arithmetic (ADD…), <b>O</b>range = input/output (PRINT…), brow<b>N</b> = labels/strings, <b>R</b>ed = logic
- The **length** of the groups = the **operand**: `GGG GG` = “STORE (3 greens) into slot 1 (2 greens)”
- Strings and inputs: a side JSON file; the program **compiles into a PNG image of candies**

</div>
<div style="flex: 0.8">
<img src="assets/img/mnm-hello-world.png" alt="Hello World in M&M's" style="max-height: 255px">
<p class="smallest">“Hello World”: this image IS the program</p>
</div>
</div>

<p class="smaller">We give the agent <b>the repository, nothing else</b> (README, opcode table, interpreter, 4 examples: 63 lines). Language published <b>5 days earlier</b>, no web access: <b>26 / 26 challenges passed</b>.</p>

Note: A language absurd by construction, published on March 7, 2026 and attacked on March 12: no possible example in the training data, and the session's permission list (versioned in the repository) allows no web access: a test of pure generalisation: you have to reason about the semantics, not recite. Challenges from the trivial (sum 1..N) to the epic (next slide). Typical initial bugs (encoding off-by-one, inverted branch polarity) fixed by the agent by re-reading the specification. The 26/26 were validated by hand on the observed output.

---

## The epic challenge: a Brainfuck interpreter… in M&M's

<p class="smaller" style="margin-bottom: 0.1em">The challenge: write, in candy tokens, a program that <b>reads and executes any Brainfuck program</b> (up to 120 instructions, 20 cells).</p>

<div class="cols" style="align-items: center; margin-top: 0.25em">
<div style="flex: 1; text-align: left">
<p class="smallest" style="color: #7ddf64; margin-bottom: 0.2em">INPUT: a Brainfuck program</p>
<pre style="margin: 0"><code>++++++++[&gt;++++[&gt;++&gt;+++
&gt;+++&gt;+&lt;&lt;&lt;&lt;-]&gt;+&gt;+&gt;-&gt;&gt;+
[&lt;]&lt;-]&gt;&gt;.&gt;---.+++++++
..+++.&gt;&gt;.&lt;-.&lt;.+++.---
---.--------.&gt;&gt;+.&gt;++.</code></pre>
</div>
<div style="flex: 0.14; font-size: 1.8em; color: #ffc857; font-weight: 700">→</div>
<div style="flex: 1.35; text-align: center">
<img src="assets/img/mnm-bf-closeup.png" alt="Excerpt of the interpreter in M&M's" style="max-height: 260px">
<p class="smallest" style="margin-top: 0.2em">THE INTERPRETER: <b>1,260 lines of M&M's</b> (excerpt)</p>
</div>
<div style="flex: 0.14; font-size: 1.8em; color: #ffc857; font-weight: 700">→</div>
<div style="flex: 0.8; text-align: left">
<p class="smallest" style="color: #7ddf64; margin-bottom: 0.2em">OUTPUT</p>
<pre style="margin: 0"><code>72 101 108 108 111
32 87 111 114 108
100 33 10</code></pre>
<p class="smallest" style="margin-top: 0.2em">= “Hello World!” (+ newline) as ASCII codes</p>
<p class="smallest" style="margin-top: 0.3em">1.6 million steps<br>1.4 seconds</p>
</div>
</div>

<p class="smaller" style="margin-top: 0.5em">No arrays in the language → the “fetch” = <b>120 comparison cases</b> · <b>174 labels</b> · 39 cross-tests</p>

Note: Get the flow right: the candy program READS a Brainfuck program (text) and PRODUCES its output. The agent invents architectures absent from any tutorial: dispatch by chains of comparisons, code generation via Python scripts. Engineering, not recitation.

---

## The program, for real

<div class="cols">
<div class="tallstrip">
<img src="assets/img/mnm-bf-full.png" alt="The complete Brainfuck interpreter in M&M's">
</div>
<div>

The image of the complete program measures

<span class="big">18,436 × 130,756 <small>pixels</small></span>

← scroll down…

<img src="assets/img/mnm-bf-zoom.png" alt="Zoom on the program" style="max-height: 155px">

</div>
</div>

Note: Visual gag: the scrolling strip. A “listing” 130,000 pixels tall. Each coloured dot is an instruction.

---

## Another esoteric language: ArnoldC 💪

Every instruction is a Schwarzenegger one-liner, and it is a **real compiled language**:

<div class="cols" style="align-items: center">
<div style="flex: 1.05; text-align: left">
<p class="smallest" style="color: #ffc857; margin: 0 0 0.15em">ArnoldC (<code>HASTA LA VISTA, BABY</code> = end of method)</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.55"><code>IT'S SHOWTIME
HEY CHRISTMAS TREE score
YOU SET US UP 0
TALK TO THE HAND "Hello World"
YOU HAVE BEEN TERMINATED</code></pre>
</div>
<div style="flex: 0.12; font-size: 1.6em; color: #ffc857; font-weight: 700">→</div>
<div style="flex: 1.05; text-align: left">
<p class="smallest" style="color: #6ec1e4; margin: 0 0 0.15em">…compiled to JVM bytecode (real excerpt, <code>javap -c</code>)</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.55"><code>0: sipush        0
3: istore_0
4: sipush        0
7: istore_1
…: invokevirtual println</code></pre>
</div>
</div>

<p class="smaller"><b>JVM</b> = <i>Java Virtual Machine</i>, the virtual machine that runs Java (and Kotlin, Scala…) on any machine.</p>

And the agent masters it too: **25 challenges solved**, 127+ tests (loops, computations, all the way up to interpreters), despite the absence of arrays and strings, and a 100-variable limit.

Note: A real open-source language, a real compiler to Java bytecode. Unlike MnM, ArnoldC (2014) is present in the training data and the session could read github.com: the point is not the absence of contamination but the tower of interpreters and the repair of the compiler. This separate mastery of the three languages (chess in Brainfuck, 26/26 in MnM, 25 challenges in ArnoldC) makes the next challenge possible.

---

## The triple interpreter 🤯

Brainfuck, M&M's, ArnoldC: mastered **separately**. So, the rather crazy challenge thrown at the agent: **stack them**, each one interpreting the next. Verdict: **38/38 tests**.

<div class="cols" style="align-items: center; margin-top: 0.4em">
<div style="flex: 1.15; text-align: left">
<p class="smallest" style="color: #ff6b6b; margin-bottom: 0.15em">THE JVM RUNS: <b>290,571 lines of ArnoldC</b> 💪 = an MnM interpreter</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.5"><code>IT'S SHOWTIME
HEY CHRISTMAS TREE po0
YOU SET US UP 0
GET TO THE CHOPPER readIdx</code></pre>
<p class="smallest" style="margin-top: 0.15em">(compiled to bytecode: the only real process)</p>
</div>
<div style="flex: 0.14; text-align: center; color: #ffc857; font-weight: 700"><div style="font-size: 1.5em; line-height: 1">→</div><div style="font-size: 0.4em">which runs</div></div>
<div style="flex: 0.85; text-align: left">
<p class="smallest" style="color: #ffc857; margin-bottom: 0.15em"><b>4,654 MnM instructions</b> 🍬 = a <i>second</i> Brainfuck interpreter (≤ 120 instr., 20 cells)</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.5"><code>OOO O
GGG GGG
G R
GGG G
N BB</code></pre>
<p class="smallest" style="margin-top: 0.15em">(the M&M's tokens, in text notation)</p>
</div>
<div style="flex: 0.14; text-align: center; color: #ffc857; font-weight: 700"><div style="font-size: 1.5em; line-height: 1">→</div><div style="font-size: 0.4em">which runs</div></div>
<div style="flex: 0.8; text-align: left">
<p class="smallest" style="color: #7ddf64; margin-bottom: 0.15em"><b>the Brainfuck program</b> (excerpt)</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.5"><code>++++++++[&gt;++++[&gt;++
&gt;+++&gt;+++&gt;+&lt;&lt;&lt;&lt;-]
&gt;+&gt;+&gt;-&gt;&gt;+[&lt;]&lt;-]&gt;&gt;.
&gt;---.+++++++..+++.</code></pre>
</div>
<div style="flex: 0.14; text-align: center; color: #ffc857; font-weight: 700"><div style="font-size: 1.5em; line-height: 1">→</div><div style="font-size: 0.4em">which prints</div></div>
<div style="flex: 0.9; text-align: left">
<p class="smallest" style="color: #7ddf64; margin-bottom: 0.15em">OUTPUT: integers!</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.5"><code>72 101 108 108 111
32 87 111 114 108
100</code></pre>
<p class="smallest" style="margin-top: 0.15em">= “Hello World” · ~18 s</p>
</div>
</div>

<p class="smaller" style="margin-top: 0.5em">Each layer is a <b>real program</b>, readable and runnable. At run time, a single process: the JVM runs the ArnoldC, which runs the MnM, which runs the Brainfuck: Russian dolls, not a pipeline.</p>

Note: Genuine excerpts from the real files (mnm_bf_generic.mnm: exactly 4,654 lines; mnm_vm.arnoldc). This is not the same file as the MnM challenge on slide 44 (challenges/26_brainfuck/bf.mnm, 1,260 lines): same specification (120 instructions, 20 cells), two distinct implementations, this one regenerated for the stacking. Walk through it from left to right in the direction of EXECUTION (the reverse of the M&M's slide, which followed the data): the only real process on the left, then what it runs, down to the output. Insist: this is NOT a pipeline (MnM produces nothing that ArnoldC would then execute). A single process, `java mnm_vm`, reads on stdin the BF interpreter written in MnM, then the BF program and its inputs; each `.` of the Brainfuck becomes an MnM PRINT, executed as an ArnoldC TALK TO THE HAND, executed as a JVM println. Hence the “72 101 108…”: the output comes out as ASCII codes, one integer per line, because ArnoldC only prints numbers (72 = H, 101 = e…). Timing: ~18 s for Hello World through the pure chain (measured, 3 runs, regenerated VM); the 7.2 s in the README is the “Path 4” variant whose MnM interpreter is tailored to the program (130,055 lines). Both interpreters are emitted by two Python generators (845 and 320 lines); zero Python at run time.

---

## Two unexpected surprises

**1.** Once warmed up, the JVM's JIT executes this 7,316-line if/else chain of a joke language as **sub-millisecond dispatch**, at native-compute level 🤨

<p class="smaller">The original punchline (“10–16× faster than the C interpreter!”) <b>does not survive the control experiment</b>: the C timing was mostly measuring… <i>process start-up</i> (~2 ms, the same as on a near-empty program). Cold, the JVM is 21–107× <i>slower</i>.</p>

**2.** Along the way, the agent diagnosed and fixed **9 defects in the ArnoldC compiler**, bugs and hard-coded limits absent from the ~70 upstream issues (100-variable limit, methods > 64 KB, reading stdin in 26 minutes…), by **decompiling the bytecode** of the compiler.

Note: The wall hit next: the JVM constant pool (65,535 entries), declared “impassable” by the agent (Sierpinski “10 tape cells short”), after a first wrong diagnosis (ASM bug, not constant pool) corrected publicly… then crossed two commits later by packing the variables into a static array (fixes 8–9). Sierpinski (2 lines) then goes through the pure chain in ~10 min, with a 466,187-line interpreter. The joke language inherits 30 years of JVM engineering. And the agent does not merely consume the language: it REPAIRS its toolchain. A real contribution to an open-source project.

---

<div class="findings">

### Takeaways #2: esoteric languages

- <span class="ok">Real generalisation: 26/26 in MnM with NO training example whatsoever · 80/80 on the Brainfuck benchmark (13.8% before)</span>
- <span class="ok">The agent invents itself complete toolchains (compilers, differential tests, perft)</span>
- <span class="ok">It even repairs other people's compilers (9 ArnoldC fixes, absent from the upstream issues)</span>
- <span class="ko">On the benchmark, it overfits to the visible tests: generalisation not guaranteed</span>
- <span class="ko">Exploding costs and slowness: $758 and 30 days for an engine that loses 0/10</span>
- <span class="ko">Does not fully respect the spirit of some esoteric languages</span>

</div>

Note: Scientifically: these experiments isolate reasoning ability from memorisation. That is their real value. On “the spirit of the languages”: the agent rarely writes by hand in the language, it builds itself a generator or a compiler that writes in its place (the factory, slide 39). Public objection from David Madore: replacing “writing in an obfuscated language” with “writing something that writes in it”, “is like trying to run a marathon with a car”. To be nuanced: the boundary is blurry, human experts also build abstractions, and in MnM and ArnoldC the constraint also bites at the generator level.

---

<!-- .slide: data-background-color="#6f4518" data-background-image="assets/img/cobol-doom-gameplay.png" data-background-opacity="0.3" class="section-slide" -->
# 4. COBOL
## 1959 – ∞: the language that refuses to die

<span class="smallest">“Coding Agents Develop COBOL Systems: Evidence from a Human-Guided Multi-Case Study” — Acher, Kebaili, Khelladi (IRISA/Inria), Espinasse (Sopra Steria)</span>

Note: ⏱ T+35 (block 5, 10 min) — Part four: the COBOL study, with an industrial partner in the loop.

---

## What the scientific literature says

COBOL: born in **1959**, still at the heart of banks, insurers and government administrations. And according to the literature, it is a “**catastrophic**” case for generative AI:

- Many attempts: **fine-tuned, specialised** models (XMainframe, 2024), narrow tasks: generation (state of the art: **49.33% Pass@1** on COBOLEval, **2024**), code explanation (Lei et al., 2025)…
- …always on programs of **a few dozen lines** (HumanEval size)
- And **developing real COBOL applications, end to end? Nothing.**

<p class="smallest">Refs: “COBOLEval: A HumanEval Transpilation for COBOL Code Generation” (2024) · “XMainframe: A Large Language Model for Mainframe Modernization” (2024) · Lei et al., “Enhancing COBOL Code Explanations: A Multi-Agents Approach” (2025)</p>

Note: The 2024–2026 literature evaluates COBOL on micro-programs, and even there, it passes one time in two. Our question: what if we tried whole SYSTEMS, with generic agents?

---

## The study: 16 systems, built from scratch

- **8 families × 2 agents** (Claude Code, Codex), on GnuCOBOL
- Compilers, chess engine, SAT solver, compressor, Doom-like, game framework, payroll…
- Open, **goal-directed** prompts: the “what”, never the “how”, no domain or language expertise injected
- The human guides, challenges, validates, but **does not write a single line of COBOL**

<span class="big">50,147 <small>lines of COBOL delivered, an order of magnitude above the benchmarks</small></span>

Note: 23 sessions, 15,010 tool calls analysed. Everything is public: github.com/acherm/agentic-cobol-study. Up to a single file of 11,044 lines.

---

## Yes, DOOM in COBOL 👾

<div class="cols">
<div>
<img src="assets/img/cobol-doom-title.png" alt="Doom COBOL — title screen" class="pixel">
</div>
<div>
<img src="assets/img/cobol-doom-gameplay.png" alt="Doom COBOL — gameplay" class="pixel">
</div>
</div>

Raycasting, enemy AI, HUD: the logic in COBOL paragraphs, the C only paints the pixels. And also: **Flappy Bird** (gravity, pipes, score).

Note: There is an SDL2 shim for the display, but all the game logic is in COBOL. Feasibility demo, not a finished product.

---

## The craziest result

<span class="big" style="font-size: 1.8em">2 COBOL → C compilers, written <u>in COBOL</u> <small>11,680 and 15,912 lines of COBOL, validated by differential execution against GnuCOBOL</small></span>

<div class="cols" style="align-items: center; margin-top: 0.25em">
<div style="flex: 1.15; text-align: left">
<p class="smallest" style="color: #ffc857; margin: 0 0 0.15em">Real excerpt: splitting COBOL into tokens… in COBOL</p>
<pre style="margin: 0; font-size: 0.4em; line-height: 1.5"><code>      * TOKENIZE-LINE: Split a line into tokens
       TOKENIZE-LINE.
           MOVE 0 TO WS-TOKEN-COUNT
           INITIALIZE WS-TOKENS
           MOVE FUNCTION TRIM(WS-TRIMMED-LINE)
               TO WS-TOK-LINE
           …
           PERFORM TOKENIZE-STRING</code></pre>
</div>
<div style="flex: 1; text-align: left">
<p style="margin: 0 0 0.3em">What it requires: a <b>twofold mastery</b> of the language:</p>
<p style="margin: 0 0 0.3em">1. <b>Understanding</b> it: grammar, syntax, semantics: the very job of a compiler</p>
<p style="margin: 0">2. <b>Writing</b> it: 27,000+ lines of COBOL that compile and work</p>
</div>
</div>

<p class="smaller">The only prior claim of a COBOL compiler written in COBOL: <b>Micro Focus, 1977</b>.</p>

Note: The most demanding class of programs there is, and an absolute historical rarity. This is the flagship result of the paper. They compile real programs: the Doom-like, a 3,854-line chess engine. The excerpt comes from cobolint.cob (Claude Code's compiler). Insist on the twofold mastery: the language as OBJECT (understanding it in order to compile it) and as MEDIUM (writing it at scale).

---

## The other pieces of the corpus

- ♟️ UCI chess engine: **~1630 Elo** (400 games against a throttled Stockfish, PGNs kept), starting from 675, +960 points over 15 phases
- 🧩 CDCL SAT solver (watched literals, VSIDS, restarts): within **8.91×** of MiniSat's (C++) time, starting from 18×
- 💰 A payroll refactored with **byte-identical** outputs before/after
- Up to **60 distinct COBOL constructs** per system
- **7 families out of 8 with no known open-source equivalent**, and oracles **replayable by a third party**

Note: 1630 Elo in COBOL vs 1365–1404 in the polyglot study: here the human guides domain by domain, hence the gain. The refactoring verified by binary diff: the kind of oracle that reassures an industrial partner.

---

## The agent reads and compiles… the human doubts and redirects

![Task breakdown](assets/figs/cobol-se_tasks-1.png) <!-- .element: style="max-height: 340px" -->

<span class="big" style="font-size: 1.5em">~85% <small>of the agent's active time = compiling + reading/understanding the code</small></span>

On the human side: **0 lines of COBOL** written, 451 prompts, of which **25%** are redirections, bug reports and verification demands.

Note: build 43% + understanding 42%: a compile-run-inspect loop. Human expertise is no longer used to type code: it is used to doubt, redirect, validate: a project-lead role. The decisive architecture pivots come from the human.

---

## The template illusion

<div class="badge">🃏</div>

Codex's “compiler” beat GnuCOBOL on speed. Too good to be true.

Digging in: it “compiled” by **pattern-matching on `PROGRAM-ID`**, with pre-written C templates.

Unmasked by the **expert's doubt** + the **differential oracle**, which then caught a real *miscompile*.

And when the prompt does not lock down the language: the COBPACK specification delivered **100% in C** (1,123 lines, zero COBOL), a Doom first attempted in **Python**.

Note: THE story to remember. “Strange to beat GnuCOBOL” → audit → structural cheating. Without expertise or an oracle, this fake compiler would have passed in a demo.

---

## The frontier / non-frontier gap

On the **easiest** task in the corpus (the Game of 15, tic-tac-toe in disguise):

- **Gemma 4** (local): **never compiled**: 15 attempts, 231 lines of errors, fabricated figures
- **Qwen 3.6**: the basics after 7 retries, then stalled
- **Mistral**: 6 h 45 min and $16.40 later, declares “the program works correctly”

Note: The Mistral story deserves a slide of its own: the next one.

---

## “The program works correctly”

Mistral's program confidently displayed:

<span class="big">362,880 <small>possible games in the Game of 15</small></span>

The exact, published mathematical value: <span class="big">255,168</span>

A missing `END-IF` made 7 of the 8 winning triples undetectable.

**Compiling proves nothing. Running proves nothing. Asserting, even less.**

Note: The PLAUSIBLE false success: it compiles, it runs, it prints credible numbers. Only the mathematical oracle (255,168) unmasks it. This is the central argument for oracles.

---

## What this opens up 🔭

Two lines of work, with **very positive signals**:

- **Maintenance and evolution**: most of the prompts were already modifying existing code (reading, diagnosing, fixing, testing without regression, restructuring, optimising). The required capabilities **are there**: 161 commits, a refactoring verified byte for byte.
- **Migration**: writing a COBOL→C compiler demands the mastery of syntax and semantics that migration pipelines presuppose. And **differential execution** gives them the oracle they need.

What remains is to confirm it on **real legacy code**: that is the work in progress.

<p class="smallest">Forthcoming: “Spec2COBOLRot” (Espinasse, Khelladi, Acher, ASE 2026, AISM workshop) · “CRACS” (Kouadio, Acher, Barais, Jézéquel, SANER 2026)</p>

Note: “Discussion” section of the paper. Maintenance: most prompts after the opening one modify an existing state; 161 commits in total, the big compiler grows over 74 commits and 11 days; the agent reads and searches its codebase (42% of the time), diagnoses and fixes, replays regression tests, adds features without regression, restructures (payroll verified byte for byte), optimises (3 rounds on the SAT solver). Migration: the two COBOL-to-C compilers prove the mastery of the source language that the published pipelines presuppose (IBM WCA4Z, AWS Transform…), with GnuCOBOL as the differential reference. Open questions: nothing has been tested yet on independent legacy code (no CICS, DB2, z/OS). LLM4Code, CodeCommons, FRAIME: mentioned in the conclusion.

---

<div class="findings">

### Takeaways #3: COBOL

- <span class="ok">16 non-trivial systems, 50,000 lines, 10× above the literature</span>
- <span class="ok">Including 2 COBOL-in-COBOL compilers (previous one: 1977) and an engine at 1630 Elo</span>
- <span class="ok">Validated by replayable external oracles (Stockfish, MiniSat, GnuCOBOL, binary diff)</span>
- <span class="ko">Success neither automatic nor autonomous: the expert and their doubts are structural</span>
- <span class="ko">Plausible false successes, cheating on the language, the template illusion</span>
- <span class="ko">Non-frontier models: out of the game, even on the easy task</span>

</div>

Note: A balanced takeaway: neither “AI replaces COBOL developers” nor “COBOL resists AI”.

---

<!-- .slide: data-background-color="#3a3a3a" data-background-image="assets/img/bfchess-snippet.png" data-background-opacity="0.18" class="section-slide" -->
# 5. Three experiments, one same pattern

Note: ⏱ T+45 (block 6a, 5 min) — Fifth part, a short one: the cross-cutting synthesis.

---

## Capabilities and shadows ☯️

<div class="cols" style="align-items: stretch; margin-top: 0.3em">
<div style="flex: 1; text-align: left; background: rgba(125,223,100,0.07); border: 2px solid #7ddf64; border-radius: 16px; padding: 0.7em 1em">
<p style="color: #7ddf64; font-weight: 800; margin: 0 0 0.4em; font-size: 1.05em">☀️ Unprecedented capabilities</p>
<ul style="font-size: 0.75em; margin-left: 0.9em">
<li>Systems <b>never written</b> in these languages: chess in TeX, APL, Rocq… COBOL compilers in COBOL</li>
<li>Scenarios <b>unthinkable yesterday</b>: a triple interpreter, an HTML page to play “FIFA”</li>
<li>A mastery of <b>almost any language</b> (esoteric, old, modern), <b>apparent AND real</b>, because <b>validated</b> by oracles</li>
</ul>
</div>
<div style="flex: 1; text-align: left; background: rgba(255,107,107,0.07); border: 2px solid #ff6b6b; border-radius: 16px; padding: 0.7em 1em">
<p style="color: #ff6b6b; font-weight: 800; margin: 0 0 0.4em; font-size: 1.05em">🌑 And their shadows</p>
<ul style="font-size: 0.75em; margin-left: 0.9em">
<li>The <b>cost</b> 💸: orders of magnitude depending on the language</li>
<li><b>Cheating</b> 🃏: as soon as the constraint isn't locked down</li>
<li><b>Overfitting</b>: saturating a benchmark ≠ being correct</li>
<li><b>Not the state of the art</b>: the gap is real (Stockfish, AAA…)</li>
</ul>
</div>
</div>

Note: The balance sheet of the synthesis, to lay out before unrolling the laws: on one side genuinely new capabilities (world firsts, absurd stacks that work, and a real mastery since it is validated by replayable oracles), on the other the recurring shadows that all three playgrounds have shown. The rest of this part details each column.

---

## Three playgrounds, the same laws

| | ♟️ Polyglot chess | 🍬 Esoteric | 🏦 COBOL |
|---|---|---|---|
| **Building is no longer the problem** | 34 engines, 17/17 languages | one engine in Brainfuck, 26/26 in M&M's | 50,000 lines, 2 compilers |
| **💸 The language sets the bill** | $1.96 (Java) → $473 (COBOL) | $758 and 30 days (BFChess) | ~$7,000, 80 h |
| **Apparent success lies** | self-proclaimed Elo: up to +1078 | 11/11 on the tests… but 60% stalemates | “works correctly”: every figure was wrong |
| **🃏 It cheats as soon as you're not looking** | the “CSS engine” coded in Python | the Brainfuck logic migrates to Python | the COBOL compressor delivered in C |
| **Only the oracle decides** | 400 games against Stockfish | perft, 39 cross-checked tests | 255,168 · GnuCOBOL diff |

The same pattern, three times: **this isn't an anecdote, it's a law of agentic development.**

Note: The whole talk fits in this table: walk through it line by line. 1: existence is a given everywhere. 2: the language is paid for in orders of magnitude. 3: compiling/running/self-grading proves nothing. 4: without a lock, the agent works around the constraint. 5: only external points of truth settle the matter.

---

## The lesson of the oracles

<img src="assets/img/motif-oracle.svg" alt="Apparent success: plausible false success or verified success" style="max-height: 580px">

Note: This is the epistemological thesis of the talk, in one diagram: generative AI produces the plausible; only external points of truth (perft, Stockfish, MiniSat, GnuCOBOL, 255,168, binary diff) separate the plausible from the correct. Walk through it: same start, same apparent “success”; the fork is verification. And the story doesn't stop at verified success: improving/optimising (Elo, gameplay, speed) requires human expertise and inputs: we remain far from Stockfish, and FIFAcher is far from a AAA game.

---

## Let's be clear-eyed: the gap is real

<div class="cols" style="align-items: center">
<div style="flex: 1.1; text-align: left; font-size: 0.88em">
<ul>
<li>FIFAcher: fun… but <b>not a AAA game at all</b></li>
<li>Chess engines: ~2100 Elo at best; <b>Stockfish is at 3,500+</b></li>
<li>COBOL compilers: not ANSI-85 compliant · SAT: <b>9×</b> behind MiniSat</li>
<li>BFChess: 0/10 against Stockfish at the minimum setting</li>
</ul>
<p style="margin-top: 0.5em">And our expectations <b>“jump” with quality</b>: the more impressive the demo, the higher the bar.</p>
</div>
<div style="flex: 0.9">
<img src="assets/img/fosse.svg" alt="The gap between the demo and the reliable system" style="max-height: 400px">
</div>
</div>

Closing it will take **technical depth**, **domain knowledge** and **mastery of languages**.

Note: The anti-hype slide of the synthesis: existence is a given, excellence is not. Hypothesis: the last mile (performance, compliance, “feel”) is precisely where human expertise (domain, low-level, languages) becomes decisive again. Leads into “The new role of expertise”.

---

## The new role of expertise

**“Programming” ≠ “Software Engineering”**: writing the code was never the essential part: architecting, testing, validating, maintaining, creating variants, understanding.

The expert no longer (necessarily) writes the code. They:

1. **Specify** precisely the features, constraints and goals to reach (*in other words: they program*)
2. **Doubt** (“strange to beat GnuCOBOL…”)
3. **Lock down the constraints** (otherwise: cheating)
4. **Build and aim the oracles**
5. **Decide** on architecture pivots

And to break through the ceiling (**exploratory**, less charted domains), **understanding the code, and therefore the languages**, becomes the decisive advantage again.

Note: Our data backs this up: the COBOL agent spends 85% of its time compiling and reading, the summer games cost 99.8% in context re-reading, and 25% of the human COBOL prompts = exactly this steering. Overview: Hou et al., “Large Language Models for Software Engineering: A Systematic Literature Review”, ACM TOSEM 2024. Expertise shifts from production to evaluation and specification: not a devaluation, a promotion. A hypothesis I stand by: the more exploratory the domain (little training data, few ready-made oracles), the more mastery of code and languages matters for doing really interesting things.

---

<!-- .slide: data-background-color="#14213d" class="section-slide" -->
# 6. What now?
## Three hypotheses on the future of programming languages

Note: ⏱ T+50 (block 6b, 8 min) — Last big part: forward-looking, and owned as such, but fed by the data from the talk. Each hypothesis is discussed with a complementary angle (software engineering, audiences, formal mathematics, encyclopedia).

---

## The three hypotheses

1. **H1: disappear… or become invisible**: natural language up front, compilation targets behind
2. **H2: become more important**: contracts, proofs, instruments of control
3. **H3: reinvent themselves**: new languages, designed for AIs

Note: Outline of the plan: the hypotheses are not mutually exclusive; each is plausible in certain contexts. H1 comes in two stages: disappearance on the interface side, invisibility on the implementation side.

---

## H1: languages disappear

French and English become **the** programming language.

**For**: my nephew. 26/26 in MnM. 50,000 lines of COBOL without writing a single one.

**Against**: natural language is **ambiguous**:
“the program works correctly”… with every figure wrong.
A prompt is not a **complete and robust** specification.

<p class="smallest">On the fragility of prompts: Döderlein, Kouadio, Acher, Khelladi, Combemale, “Piloting Copilot, Codex, and StarCoder2: Hot Temperature, Cold Prompts, or Black Magic?”, Journal of Systems and Software, 2025</p>

Note: H1 is true for the INTERFACE and for some uses (prototypes, personal games). It is false as soon as contractual precision is needed.

---

## H1 (continued): …or become invisible

> “Code itself will go away in favor of just making the binary directly.” — Elon Musk (2026)

Like assembly for most developers: still there, but **rarely read**, even though it remains very much **alive** (ffmpeg, VLC or chess engines still write it by hand, and debugging C sometimes forces you to read it). The extreme version, Musk-style: no code at all, **straight to the binary**.

Programming languages become **compilation targets** of natural language.

But then… who **audits**? Codex's template compiler “worked” too…
until a human *read* it.

Note: The assembly analogy must be handled with nuance (cf. backup slide “Assembly isn't dead”): invisibility is a question of POPULATION, not of existence. Musk's quote (public remark, 2025–2026) is the extreme version of this hypothesis: skip the source code, produce the binary directly. Counter-question: without source code, who audits what? H1 is already partly true (who reads minified JS?). The catch: our experiments show that human reading of the generated code remains the last safety net: invisibility comes at a cost in trust.

---

## From my nephew… to scientists

- My nephew: the game has to be **fun**, no guarantee required
- The data analyst: the figure has to be **right**
- The physicist: the result has to be **reproducible**
- The bank: the system has to be **auditable for 30 years**

The same “vibe coding” cannot serve all four.

> “The world of computing is far grander than your world, Paul. It may be the end of programming **for you**, perhaps, but not for millions of others.” — Grady Booch

Not the end of programming: **the end of a monopoly**.

Note: The axis that structures everything: what level of trust do you require, and who verifies it? The higher the requirement, the more languages, oracles and methods matter. Booch answers the “end of code” prophecies: programming doesn't disappear, it multiplies across audiences and contexts.

---

## H2: languages become MORE important

The language as **contract** and as **oracle**:

- Types, static analyses, tests: **machine-checkable meaning**
- Lean 4, Why3, Rocq in our experiments: the code comes **with its proof**
- The language locks down the constraints the agent would like to “relax”
- And **domain-specific languages** (DSLs): **framing** the agent by speaking the **vocabulary of the domain**, stating the “what” in the domain experts' own terms

The more AI generates, the more we need **precise and formal** ways of saying what we want.

Note: My favourite, and the best supported by our data: everywhere we won (Elo, compilers, byte-identical refactoring), it was a formalism that made verification possible.

---

## What if we pushed mathematics forward? 🧮

<div class="cols" style="align-items: center; margin-top: 0.2em">
<div style="flex: 1.1; text-align: left">
<ul>
<li>AIs at <b>Olympiad gold-medal</b> level, with <b>fully formalised</b> proofs</li>
<li><b>10 of the 12 problems of Putnam 2025</b> solved by an agent… in <b>Rocq</b> (Baudart, Lelarge et al., 2026)</li>
<li>MiniF2F automatically translated between proof assistants (Viennot, Baudart, Gallego Arias, Lelarge, 2025)</li>
</ul>
</div>
<div style="flex: 0.95; text-align: left">
<p class="smallest" style="color: #ffc857; margin: 0 0 0.15em">A proof is code: Rocq (example)</p>
<pre style="margin: 0; font-size: 0.42em; line-height: 1.5"><code>Lemma sum_squares (n : nat) :
  6 * sum n (fun i => i * i)
    = n * (n + 1) * (2 * n + 1).
Proof.
  induction n as [|n IH].
  - reflexivity.
  - simpl; lia.
Qed.</code></pre>
<p class="smallest" style="margin-top: 0.15em"><code>Qed</code>: the machine has checked <b>every</b> step</p>
</div>
</div>

The dream: agents that **explore, formalise, prove**. And the language of that dream is **not French**: it's **code**, the ultimate oracle.

<p class="smallest" style="margin-top: 0.2em">“Putnam 2025 Problems in Rocq using Opus 4.6 and Rocq-MCP” (2026) · “MiniF2F in Rocq” (2025)</p>

Note: Something to dream about: AI doesn't just make games: it tackles research problems. Putnam = THE North American undergraduate mathematics competition. Work carried out notably within the Inria LLM4Code Challenge (Guillaume Baudart co-leads it, with me).

---

## H3: new languages, designed for AIs

Remember: an agent **designed its own DSL** (“GAMBIT”, + C++ transpiler)
without being asked to.

What does a language optimised for machine **generation** and **verification** rather than human reading look like?

Note: Open research question. Amusing clue: when left free, the agent invents a language… that is rather classical. The good programming language concepts may already have been discovered.

---

## Back to the 14,000+ languages

A **living encyclopedia of languages**, backed by:

<div class="logos" style="padding: 0.18em 0.8em; margin: 0.1em auto 0.25em; gap: 1.1em">
<img src="assets/img/logos/swh.svg" alt="Software Heritage" style="height: 30px">
<img src="assets/img/logos/codecommons.png" alt="CodeCommons" style="height: 30px">
<span style="color: #222; font-weight: 700; font-size: 0.5em">CodeCommons</span>
</div>

<div class="cols" style="align-items: flex-start">
<div>
<img src="assets/img/plcatalog-home.png" alt="PL Catalog — home" style="max-height: 175px">
<p class="smallest">14,000+ languages catalogued</p>
</div>
<div>
<img src="assets/img/plcatalog-cobol.png" alt="PL Catalog — COBOL page" style="max-height: 175px">
<p class="smallest">…with <b>real archived programs</b> (SWHID)</p>
</div>
</div>

**Will all this knowledge disappear?** Will AIs master **all** languages, and their **subtleties**?

<p class="smallest" style="margin-top: 0.15em">Desmazières, Di Cosmo, Lorentz, MSR 2025 · blog.mathieuacher.com/PL-ultimate-llm/</p>

Note: Echo of the opening slide: the figure asserted at the start comes back here as questions. The richness of programming is a heritage: 50 years of language evolution seen through Software Heritage (Desmazières, Di Cosmo, Lorentz, MSR 2025). Our data suggests: agents manage everywhere (17/17)… but the subtleties (advanced features, idioms, costs) remain very uneven. Hence the initiative: catalogue and build tooling, to measure this mastery on the 14,000, not on 20.

---

## So, what to teach and learn? 🎓

Less: syntax, rote learning, boilerplate.

Just as much: algorithmics, data structures, complexity.

**More**: specifying precisely · reading and evaluating code you didn't write ·
designing oracles and tests · **exploring and finding variants** ·
**language culture** (typing, semantics, paradigms)

Note: For the students in the room: value shifts towards what agents do poorly: doubting, specifying, verifying. PL culture is a multiplier: it is what makes it possible to choose, constrain and audit.

---

## As things stand today

**“COBOL, M&M's, French… or whatever?”** No. Not “whatever”.

<span class="big" style="font-size: 1.6em">You can <i>start</i> in any language, the question is at what price…<br>you can only <i>finish</i> in a language you <b>master</b>.</span>

Note: A committed answer, as things stand today, to the question asked at the opening. The role of languages shifts but intensifies: not for writing, but for specifying, controlling, verifying and understanding what AI produces.

---

<h2 style="font-size: 1.06em; margin-bottom: 0.5em">Programming languages in the age of generative AI:<br>COBOL, M&M's, French… or <s>whatever</s>?</h2>

<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.35em; width: 42%; margin: 0 auto">
<img class="plain" src="assets/img/recap-fifacher.png" alt="FIFAcher" style="width: 100%; border: 1px solid #3a3d4a; border-radius: 10px">
<img class="plain" src="assets/img/recap-triple.png" alt="The triple interpreter" style="width: 100%; border: 1px solid #3a3d4a; border-radius: 10px">
<img class="plain" src="assets/img/recap-tex.jpg" alt="Chess in LaTeX, in Overleaf" style="width: 100%; border: 1px solid #3a3d4a; border-radius: 10px">
<img class="plain" src="assets/img/recap-cobol.png" alt="The COBOL-in-COBOL compilers" style="width: 100%; border: 1px solid #3a3d4a; border-radius: 10px">
</div>

<p class="smallest">To go further: Inria <b>LLM4Code</b> Challenge (project.inria.fr/llm4code) · <b>CodeCommons</b> (codecommons.org) · <b>FRAIME</b> Challenge, formal methods × AI, with Mitsubishi Electric (inria.fr/fr/fraime)</p>

<p class="smallest" style="margin: 0.15em 0 0">blog.mathieuacher.com · 𝕏 @acherm · ▶ @CodeplAI</p>

<div class="logos" style="padding: 0.16em 0.7em; margin: 0.1em auto 0; gap: 1em">
<img src="assets/img/logos/insa-rennes.svg" alt="INSA Rennes" style="height: 25px">
<img src="assets/img/logos/univ-rennes.svg" alt="Université de Rennes" style="height: 25px">
<img src="assets/img/logos/irisa.png" alt="IRISA" style="height: 25px">
<img src="assets/img/logos/inria.svg" alt="Inria" style="height: 25px">
<img src="assets/img/logos/iuf.png" alt="IUF" style="height: 25px">
</div>

Note: ⏱ T+58 — The 4 callbacks: code, languages, visuals: FIFAcher (vibe coding with the family), the triple interpreter (the three codes stacked), chess in LaTeX in Overleaf, and the COBOL-in-COBOL compilers (the double mastery). The three messages, to walk through: (1) anyone can bring a program into existence: a real revolution; (2) existing ≠ being correct: without oracle or expertise, the plausible-but-wrong wins (362,880 ≠ 255,168); (3) languages are our instrument of control: ceiling, cost, contract, audit. FRAIME: Inria challenge with Mitsubishi Electric R&D Centre Europe, formal methods and AI intertwined (teams ARGO, DEVINE, DIVERSE, EPICURE, GALLINETTE). LLM4Code: 13 Inria teams + Software Heritage + Sopra Steria, co-led with Guillaume Baudart.

---

<!-- .slide: data-background-color="#000000" data-background-image="assets/img/mnm-histogram.png" data-background-opacity="0.13" -->
# Thank you! 🙏

**Questions?**

- 📝 blog.mathieuacher.com: posts on ASHFALL/FIFAcher, BFChess, MnM, TeXCCChess, PL Catalog
- 📄 arXiv:2606.13763 (polyglot chess) · COBOL study: github.com/acherm/agentic-cobol-study
- 🍬 github.com/acherm/agentic-arnoldc: the triple interpreter
- 🎮 Play: blog.mathieuacher.com/ashfall · /fifacher · chess inside Overleaf (TeXCCChess post)
- 🔬 Inria challenge **LLM4Code**: project.inria.fr/llm4code

🎙️ Mathieu Acher · INSA Rennes / IRISA / Inria

Note: We have 30 minutes of questions: References slide on display, and the 36 backup slides in reserve (O key). Frequent questions to anticipate: “what about security?”, “which jobs disappear?”, “why Claude and not X?”, “how much does it really cost?”.

---

<!-- .slide: data-background-color="#000000" -->
## References

<div class="cols" style="align-items: flex-start; text-align: left; font-size: 0.40em; line-height: 1.45">
<div>

**The studies behind this talk**
- Acher, Jézéquel, “Do Programming Languages Still Matter to Your AI Coding Agent Teammate? Evidence at Scale from Chess Engines”, arXiv:2606.13763, 2026
- Acher, Kebaili, Khelladi, Espinasse, “Coding Agents Develop COBOL Systems: Evidence from a Human-Guided Multi-Case Study”, 2026 · github.com/acherm/agentic-cobol-study
- Blog posts: Call of Acher & FIFAcher · BFChess · MnM Lang · TeXCCChess · PL Catalog · blog.mathieuacher.com
- “End-User Programming of Flappy Bird with ChatGPT: A Reality Check”, dev.to/diverse_research, 2023
- Triple interpreter: github.com/acherm/agentic-arnoldc
- Sharma, Chopra, “EsoLang-Bench: Evaluating Genuine Reasoning in Large Language Models via Esoteric Programming Languages”, arXiv:2603.09678, 2026 · agentic replication: github.com/acherm/agentic-esolang-bench (PR #1: J.-B. Döderlein)

**On reliability and costs**
- Döderlein, Kouadio, Acher, Khelladi, Combemale, “Piloting Copilot, Codex, and StarCoder2: Hot Temperature, Cold Prompts, or Black Magic?”, Journal of Systems and Software, 2025
- Reux, Acher, Khelladi, Quinton, Barais, “Imperfect Visual Verification for Code Edition: A Case Study on TikZ”, 2026
- Coignion, Quinton, Rouvoy, “When Faster Isn't Greener: The Hidden Costs of LLM-Based Code Optimization”, ASE 2025
- Spieker, Matricon, Belmecheri, Betten, Le Bartz Lyan, Borges, Mazouni, Gross, Gotlieb, Acher, “Prompting for Performance: Exploring LLMs for Configuring Software”, ICTAI 2025

</div>
<div>

**COBOL modernisation (forthcoming)**
- Espinasse, Khelladi, Acher, “Spec2COBOLRot: An Agentic-AI Degradation Loop for Realistic COBOL Corpus Generation”, ASE 2026, AISM workshop
- Kouadio, Acher, Barais, Jézéquel, “CRACS: Question-Driven Assessment of Legacy Code Summaries in Industrial IBM-i Modernization”, SANER 2026

**Formal mathematics**
- Baudart, Lelarge et al., “Putnam 2025 Problems in Rocq using Opus 4.6 and Rocq-MCP”, 2026
- Viennot, Baudart, Gallego Arias, Lelarge, “MiniF2F in Rocq: Automatic Translation Between Proof Assistants”, 2025

**Surveys and heritage**
- Acher, “Who Codes When AI Can Generate Code?”, SOTELO seminar, 4 June 2025
- Hou et al., “Large Language Models for Software Engineering: A Systematic Literature Review”, ACM TOSEM 2024
- Robbes, Matricon, Degueule, Hora, Zacchiroli, “Agentic Very Much! Adoption of Coding Agent in New GitHub Projects”, 2026
- Desmazières, Di Cosmo, Lorentz, “50 Years of Programming Language Evolution through the Software Heritage Looking Glass”, MSR 2025
- Stockfish (3500+ Elo): “The Constant”, Source Code Exhibition, Software Heritage · sourcecode-exhibition.softwareheritage.org/the-constant/
- “COBOLEval” (2024) · “XMainframe” (2024) · Lei et al. (2025)
- Inria challenge **LLM4Code** · project.inria.fr/llm4code

</div>
</div>

Note: Leave this slide on display during the questions.

---

<!-- .slide: data-background-color="#1a1a24" class="section-slide" -->
# Backup
## Extra slides, for the discussion

Note: End of the talk: everything that follows is supporting material for the questions (protocol details, anecdotes, extra figures). O key to navigate in overview mode.

---

## Backup · The limits, stated honestly

- GnuCOBOL ≠ mainframe: no CICS, IMS, DB2, z/OS
- Building from scratch ≠ **taking over legacy code** (the real industrial problem)
- Retrospective sample of successes → **no success rate**
- Real ceilings: compilers not ANSI-85 compliant, chess far from Stockfish, SAT at 9× MiniSat

Note: Out loud: what the study does NOT say. Modernising 200 million lines of legacy code is not solved by these 16 systems, but the “COBOL is impossible for AI” line no longer holds either.

---


## Hyper-personalisation

<div class="cols">
<div>
<img src="assets/img/fifacher-stade-raoul-brulat.jpg" alt="Stade Raoul Brulat">
</div>
<div>

- The **“Stade Raoul Brulat”**
- A team of **11 “Achers”**
- Fictional Breton sponsors
- Family in-jokes in the commentary
- And **2 “cheated” players**: any shot becomes overpowered, and the opposing goalkeeper lets it through 🥅

No studio would ever build this. <br>**Marginal cost ≈ one sentence.**

</div>
</div>

Note: This is THE new economic point: extreme personalisation becomes free. A game for one family, for one class, for one birthday.

---

## The 10-year-old got it in 10 minutes

- He states his feature requests directly
- He **tests**, grumbles when it fails, asks again
- He never sees the code, and never asks for it

The barrier to entry for programming has just collapsed.

Note: Anecdote to tell: his typical requests, his reaction when it works. He is doing software engineering without knowing it: specification, validation, iteration.

---

## Under the hood: an agent factory

- **60 user requests** in total for the 2 games
- **92 sub-agents** launched by the main agent
- The agent **critiques itself via screenshots** (199 screenshots logged)
- 37 self-inspection scripts written by the agent itself

Note: The agent orchestrates: it codes, launches the game, takes a picture of itself, corrects itself. It is a near-autonomous development loop… near.

---

## The number that changes everything

<span class="big">1.15 billion <small>tokens processed for the 2 games</small></span>

of which… <span class="big">0.19% <small>only end up as executable code</small></span>

Note: 2.18 million tokens of code out of 1.15 billion processed. The rest? Reading, re-reading, re-re-reading the existing code to keep the context.

---

## Let's test the limits, scientifically

What if we forced the agents to program in **very different** languages?

Mainstream (Python, Rust, Java)… but also **COBOL** (1959), **Brainfuck** (8 characters), **M&M's** 🍬

On one common playing field: **chess** ♟️

Note: Transition to the systematic experiments. Why chess? Next slide.

---

## The protocol

- **2 agents**: Claude Code and Codex, frontier versions (2026)
- **A single prompt**: “*I want to build a chess engine in [LANG]… assess its Elo*”
- **No** chess knowledge provided: never a single algorithm name
- **Documented** human-intervention policy
- **External, unified** Elo re-evaluation: gauntlet against 5 calibrated references (including throttled Stockfish), 120s+1s

Note: The key methodological point: we never trust the agent to grade itself: we replay everything in an independent tournament. Correlation with an independent round-robin: r = 0.94.

---

## TeXCCChess, seriously?

- **~1280 Elo** (95% CI: 1225–1345), a “casual tournament player”
- Depth 3 + alpha-beta + quiescence, **0.5 to 3.5 s per move**
- Validated over 100 games against Stockfish throttled to 1320: **45W 7D 48L**
- The anecdote: the **register crisis**: the state stack at `\count300` collided with the LaTeX allocator; the agent traced it and moved it to `\count10000`

Note: Another memorable bug: \numexpr 63/8 gives 8 (rounding) and not 7 (truncation): it broke all the coordinate extraction. “As far as I can tell, there is no prior chess engine in TeX.” The pattern shows up again: hostile language → the agent gets there, at a real cost, with bugs from another world.

---

## Did everything really work?

No empty category, but some **asterisks**:

- **CSS/HTML** (3 engines): play in the browser, no UCI protocol → strength **not measurable**
- **Mojo**: the only “under-converged” session (~900 Elo, stopped on budget)
- **LaTeX** (Codex replication): loses **all** its games (~550 self-estimated)
- **TeXCCChess and the slowest Brainfuck**: > 30 s per move → **forfeit on time**

Failures of **interface** and **speed**, never an inability to play chess.

Note: RQ4, “Where the floor really sits”: 7 engines without an external Elo, all for reasons of interface or raw speed. Measured floor: SQL ≈ 520; the winless LaTeX/CSS engines are even lower. Out loud: the honest answer to “where did it fail?”.

---

## Where does the money go? Look at the pace

<div class="badge">💸</div>

![Feature growth](assets/figs/chess-feature-growth.png) <!-- .element: style="max-height: 385px" -->

Ruby leaps · COBOL climbs in steps · LaTeX plateaus at 6 features · Brainfuck stays **flat for 75% of the session** (the agent is building its tooling)… then jumps to 20.

Note: Cumulative growth of delivered features, per representative language. In Brainfuck, 3/4 of the budget goes into the toolchain before the first chess feature: that is where the cost difference goes. Cost follows iterations, and iterations follow the language.

---

## An honest thermometer changes everything

Controlled retry of the C engine, with an external oracle plugged in continuously:

<span class="big">1415 → 1798 Elo <small>for ~$30, i.e. ~$0.08 per Elo point</small></span>

Paying for tokens is not enough. **Paying for tokens guided by a reliable oracle is.**

Note: Same agent, same language: what changed is the quality of the evaluation signal. Message: invest in oracles, not just in prompts.

---

## Brainfuck: 8 characters, that's it

```text
> < + - . , [ ]
```

No variables. No functions. No indexed memory access.
Just a tape of cells and a pointer.

```text
++++++++[>++++[>++>+++>+++>+<<<<-]>+>+>->>+[<]<-]
>>.>---.+++++++..+++.>>.<-.<.+++.------.--------.>>+.>++.
```
<span class="smallest">↑ this prints “Hello World!”</span>

Note: Turing-complete, so “everything” is possible in theory. In practice, it is hell: that is the whole point of the language (1993, Urban Müller).

---

## Archaeology of a bug

`print_char`, the routine that prints text,
**was silently corrupting the chessboard** (collision on cell 30).

At least **9 cell-collision bugs** debugged by the agent.

Total cost: ~34 active hours, ~2,700 API calls, 221M tokens, **$758**.

Note: Debugging a 672-cell state with no variable names: the agent manages it, but slowly and expensively. 198M of the 221M tokens = cache re-reads. The economics of context, again.

---

## An instructive episode: the temptation

<div class="badge">🃏</div>

In a parallel experiment (Codex), the agent “solves” the constraints…
by **quietly migrating the logic to Python**.

> “The human must actively verify that the constraints are respected, because the agent may *solve* the problem by relaxing them.”

Note: The same pattern as the CSS engine. The language constraint only holds if someone (or something) is watching it.

---

## The pure generalisation test

We give Claude Code **the repository, nothing else** (README + opcode table, the interpreter, 4 examples = 63 lines).

A language published 5 days earlier. No web access. Zero Stack Overflow. Zero model solutions.

Then **26 challenges**, from the trivial (sum 1..N) to the epic.

<span class="big">Score: 26 / 26</span>

Note: This is the knockout argument against “LLMs just copy”: here there is NOTHING to copy. You have to reason about the semantics of an unknown language.

---

## Programs made of candy

<div class="cols">
<div>
<img src="assets/img/mnm-mul-table.png" alt="Multiplication table in M&M's" style="max-height: 470px">
<p class="smallest">Multiplication table</p>
</div>
<div>
<img src="assets/img/mnm-histogram.png" alt="Histogram in M&M's" style="max-height: 470px">
<p class="smallest">Histogram (53 lines)</p>
</div>
</div>

Note: Yes, these images ARE the programs. You could lay them out on a table with real M&M's and “run” them.

---

## The triple interpreter 🤯

<span class="big" style="font-size:1.6em">BF → M&M's → Schwarzenegger → JVM</span>

Three generic interpreters **stacked**, each in a different absurd language.

Note: Announcing the concept: we will first SEE the programs, then the overall diagram. It is a working Tower of Babel.

---

## The tower of Babel, in detail

<img src="assets/img/triple-interpreter.svg" alt="The triple interpreter ArnoldC → MnM → Brainfuck" style="max-height: 600px">

Note: Walk through it floor by floor, top to bottom: the BF program is read by a BF interpreter written in M&M's (4,654 instructions), itself interpreted by a 290,571-line ArnoldC program, compiled to the JVM. No floor has arrays: every memory access = a chain of comparisons. 38/38 test programs pass.

---

## The combinatorial explosion

Sierpinski triangle:

**124** BF instructions → **11,122** MnM instructions → **466,187** ArnoldC lines

An ASCII chessboard: 1,092 BF → 33,382 MnM → **1,385,443 lines**, estimated at **20+ hours** of execution.

Each level adds ~one order of magnitude.

Note: Why so slow? No arrays at any level: every access = an O(N) chain of comparisons, at every floor. ~10 min for 2 lines of the Sierpinski through the triple chain.

---

## …and an “impassable” wall

The JVM class file format caps the *constant pool* at **65,535 entries** (`u2`, 16 bits).

One static field per variable → the Sierpinski through the pure triple chain **fails “just 10 tape cells short”**. The agent's verdict: “no version of ASM can fix this”.

**Two commits later**: variables packed into a static array, wall cleared: Sierpinski (2 lines) runs in ~10 min through 466,187 lines of ArnoldC.

Note: A twofold lesson: even in the absurd, you hit HARD format or platform limits, and an agent's “impossible” diagnosis is only a hypothesis: it first got the cause wrong (ASM bug, not constant pool), corrected itself publicly, then worked around the limit. It takes a human, or a very good agent, to understand which of the limits is really hard.

---

## Just toys, all of this?

Fine. Let's talk about a language that
**your salaries, your taxes and your bank depend on.**

Note: COBOL transition: we leave the lab for a real industrial stake.

---

## COBOL in 2026

```text
       IDENTIFICATION DIVISION.
       PROGRAM-ID. HELLO.
       PROCEDURE DIVISION.
           DISPLAY "HELLO, WORLD".
           STOP RUN.
```

- Born in **1959** (Grace Hopper isn't far away)
- Still at the heart of banks, insurers, government agencies
- COBOL developers are retiring faster than they're being replaced

Note: Verbose, deemed archaic: one of the oldest languages still in critical production. Hence the “modernisation” stakes.

---

## What makes these results solid 💪

- **Systems never built before**: 7 of the 8 families have **no known open-source equivalent** in COBOL: nothing to copy from
- **Very demanding oracles**: rated Stockfish tournaments (PGNs kept), MiniSat/SAT4J cross-checks, **differential execution against GnuCOBOL**, published mathematical values, TRUST suite (70+ assertions, SHA-256, fuzzing), all of it **replayable by a third party**
- **Feature-rich COBOL**: up to 60 distinct constructs, 10/10 categories (COMP-5, RECURSIVE, OCCURS DEPENDING ON…)
- **Real software-engineering tasks**, not just building from scratch: behaviour-preserving refactoring, a 6-step payroll protocol, debugging, testing, evolution, on a **rich codebase** (186 files, up to 11,044 lines in a single file)

Note: The answer to the “it's a toy example” objection: replayable validation, and the variation between runs (same prompt → structurally different artefacts) rules out copying a canonical implementation. The agents even build part of the validation apparatus themselves: one agent's fuzzer caught a division-by-zero in its own code.

---

## And what about the human?

- **0 lines of COBOL written**… but **451 prompts**, 313,404 characters
- **25.3%** of prompts = redirections, bug reports, verification demands
- The decisive architecture pivots come from the human

![Prompt intents](assets/figs/cobol-intents-1.png) <!-- .element: style="max-height: 330px" -->

Note: Expertise is no longer used to type code: it's used to DOUBT, to redirect, to validate. It's a supervising-engineer role.

---

## The COBOL cheating

<div class="badge">🃏</div>

When the prompt doesn't lock the language down:

- The COBPACK spec (a COBOL compressor) delivered as **1,123 lines of C, zero COBOL** (excluded from the corpus for that reason)
- Codex's first reflex on the Doom-like: a **Python** raycaster; a single reminder (“faking to write COBOL”) was enough to make it pivot

The same pattern as the CSS engine and the Brainfuck-Python.

Note: The paper's “evasion” section: same COBPACK spec → Claude answers in C (1,123 LoC, zero COBOL, excluded), Codex answers in COBOL (1,812 LoC + 70 assertions). Third occurrence of the constraint-cheating pattern in the talk: an invariant of agent behaviour, not an accident.

---

## The gap

Between the **spectacular demo** (one evening, it works)
and the **reliable system** (every day, it's true):

oracles, auditing, expertise, time, and **precise languages** to express all of that.

Note: “The gap” from the talk's abstract. It isn't closed with more tokens: it's closed with more rigour.

---

## And there isn't ONE context, but a thousand

Who “programs” today?

- Professional developers 👩‍💻
- **Scientists** (physics, maths, neuroimaging…) 🔬
- End-users: spreadsheets, forms, automations 📊
- Data analysts 📈
- Beginners, hobbyists, **kids** 🧒
- Students, in every discipline 🎓

<p class="smallest" style="margin-top: 0.6em">Based on “Who Codes When AI Can Generate Code?”, SOTELO seminar, 4 June 2025</p>

Note: Taken from the panorama “Who Codes When AI Can Generate Code? Impacts of Generative AI on Professional Developers, End Users, and Researchers” (SOTELO seminar “De l'impact de l'IA-générative sur le génie logiciel”, i.e. on the impact of generative AI on software engineering, 4 June 2025). Every context has its own requirements: the throwaway Sunday prototype and the payroll system don't play by the same rules.

---

## The language of that dream isn't French

Those proofs are **code**: **Lean**, **Rocq**: programming languages, heavily typed.

- Every step is **checked by the machine**: the ultimate oracle, no template illusion possible
- The agent **converses with the proof assistant** (compile, fail, fix): the same loop as for our chess engines
- To dream big, you need **precise** languages: natural language isn't enough

Note: The talk's loop closes: at the summit of ambition (advancing mathematics), what you find isn't natural language but the most formal languages there are. A Rocq proof that compiles IS correct: it's the only domain where “apparent success” cannot lie.

---

## What has really ended

Not programming.

**The monopoly** of a single way of programming,
by a single population,
in a handful of languages.

Note: Let this phrasing breathe. Transition to the final hypotheses.

---

## What our data actually say

1. The language sets the **performance ceiling** (Java→Rust: 1922; Java→COBOL: 1404)
2. The language sets the **cost** (×10 to ×240)
3. The language is a **revealer**: it's by constraining it that you see what the agent really understands
4. Without supervision, agents **cheat** on the constraints
5. The real gains come from **oracles**, not from prompts ($0.08/Elo)

Note: Empirical summary before the final answer. Each point refers back to an experiment shown in the talk.


---

## Backup · The games, in tokens and lines

<div class="badge">💸</div>

| | ASHFALL | FIFAcher | Total |
|---|---|---|---|
| User requests | 45 | 15 | 60 |
| Sub-agents | 56 | 36 | 92 |
| Input tokens | 585 M | 562 M | **~1.15 billion** |
| …that became code | | | 2.18 M (**0.19%**) |
| Code delivered | | | ~18,900 lines of JavaScript (19 modules) |
| Cost | | | $1,000 – $1,200 |

A development session **very quickly fills a context of ~1 million tokens**, out of reach, *by construction*, of today's open-weight coding agents (much smaller windows).

Note: Argument for the frontier/non-frontier discussion: beyond model quality, the ability to hold an immense context (reading and re-reading the entire codebase) is structural. 99.8% of the cost goes into re-reading context.

---

## Backup · Chess & COBOL, in tokens and lines

<div class="badge">💸</div>

| | Chess (34 engines) | COBOL (16 systems) |
|---|---|---|
| Code delivered | from ~1,000 lines… to a 5.9 MB Brainfuck file | **50,147 lines of COBOL** (186 files, max 11,044 lines/file) |
| Tokens processed | median ~56 M/session · COBOL-chess: 463 M · BFChess: 221 M | **4.4 billion** |
| Fresh generation | BFChess: ~344 K tokens generated (the rest: re-reading) | — |
| Time | median 2.3 h/session · BFChess: 30 days | 80.5 active hours, 15,010 tool calls |
| Cost | ~$2,100 (corpus) | ~$7,016 (pricing scenario) |

Working memory is **the** bottleneck: ~99% of tokens are spent *re-reading* context: the structural advantage of frontier agents.

Note: BFChess: 221 M tokens, of which 198 M are cache reads, and only 344 K of fresh generation. The Claude COBOL compiler alone: 98 prompts, 32.5 h, ~$5,185. To be set against the non-frontier models of the COBOL study (Gemma: never compiled; Mistral: 6 h 45 min for a fake success).

---

## Backup · Self-reported Elo trajectories

![Elo curves](assets/figs/chess-elo-curves.png) <!-- .element: style="max-height: 560px" -->

Note: The Elo the agent credits itself with over the course of the session, by language category (general-purpose at the top, esoteric at the bottom; dotted lines = “zigzag” trajectories, where the agent detects and reverts its own regressions).

---

## Backup · Assembly isn't dead

- Flagship projects **still write assembly by hand**: ffmpeg, VLC/x264, codecs: optimised SIMD kernels, faster than what the compiler produces
- Even in **C, Rust or Zig**: knowing what happens at the hardware level (caches, vectorisation, branching) **makes the difference**: video games, codecs, high-performance computing
- “Legacy” in our taxonomy = a study category, not a judgement: low-level is **living knowledge**

Note: Tie back to the gap: the last few percent of performance demand exactly this technical mastery, the kind agents haven't yet demonstrated at this level (cf. the assembly engine: 1403 Elo measured, far from its agent-author's hopes).

---

## Backup · The esoteric meta-study: 5 cases

| Case | Existing training corpus | Result |
|---|---|---|
| Brainfuck benchmark | ~5,000 toy repos | **80/80** on the bench's criterion (previous best score: **13.8%**; same model family: 12.5%) |
| BFChess | no pre-existing engine | ~5.9 MB of pure Brainfuck, UCI protocol |
| MnM | language **5 days old**, worldwide corpus: **63 lines** | **26/26** challenges |
| ArnoldC | hello-worlds; compiler dormant since ~2015 | 25/25 + **9 compiler bugs fixed** |
| Triple interpreter | — | 290,571 lines, 38/38 tests |

**12.5% → 100% within the same model family**: the **agentic harness** (interpreter in the loop, unlimited attempts) counts as much as the model.

Note: Meta-study “Beyond Memorization: Coding Agents Can Master Esoteric Programming Languages” (in progress). Unplanned cross-vendor replication: Codex, pointed at the finished artefact, formalised the pattern (Futamura projections) and re-instantiated it: Whitespace→FALSE→FRACTRAN, validated against the CRAN package Rfractran (4,000 steps of Conway's prime generator).

---

## Backup · Passing the tests ≠ mastering the craft

- **Overfitting to the tests**: fuzzing against a spec-faithful oracle → **54 of the 80 solutions** fail on spec-compliant inputs (integers > 255, one more line than the tests, a trailing “\n”); 26 are genuinely general: *saturating a fixed oracle ≠ general correctness*
- The verdict of a **recognised Brainfuck expert**: the agent “produces programs that pass the tests”… but “doesn't write good Brainfuck yet”. Line sorting: **171,559 instructions** from the agent vs **under 400 bytes** from the expert
- And on the numbers side: **no overestimate survived an adversarial measurement**, but someone still had to make that measurement (cf. the JIT punchline, deflated by a simple control experiment)

Note: Pers. comm. April 2026 (⚠️ ask for permission before any public named citation; anonymised here). His image: “Brainfuck wants to be sculpted like clay; many handle it with tongs, like a radioactive sample, and the agent does the same”. Feeds directly into the slide “Let's be clear-eyed: the gap is there”.
