# Langages de programmation à l'ère de l'IA générative : COBOL, M&Ms, français… ou peu importe ?

Talk de Mathieu Acher (INSA Rennes), slides reveal.js en Markdown.

**🌐 En ligne (auto-contenu, vidéos comprises) : https://blog.mathieuacher.com/languages-codingagents-semaineIA2026/**
(version longue : https://blog.mathieuacher.com/languages-codingagents-semaineIA2026/long.html)

Vendredi 4 septembre 2026 · Semaine de l'IA · Université de Rennes ·
https://intelligence-artificielle.univ-rennes.fr/semaine-ia-2026

## Résumé

À l'ère de l'IA générative et du *vibe coding*, programmer peut commencer par une simple description
en langue naturelle, en anglais ou en français, de ce que l'on souhaite obtenir. Des agents de codage
peuvent aujourd'hui produire des sites web, des jeux, des solveurs, voire des compilateurs ou des outils
plus ambitieux, avec des résultats parfois impressionnants. Pour tester leurs limites, on peut les
confronter à des langages très différents : Python, Rust ou JavaScript, mais aussi COBOL, l'un des plus
vieux langages encore utilisés, Brainfuck, un langage composé de seulement 8 caractères, ou même un
langage à base de M&Ms.

Ces expériences donnent lieu à des démonstrations étonnantes : un jeu DOOM en COBOL, un jeu d'échecs
en Brainfuck ou des programmes non triviaux écrits avec des bonbons colorés. L'intérêt est que ces
programmes ne sont pas de simples copies retrouvées quelque part : ils sont générés à chaque fois, avec
leurs propres choix, leurs surprises, leurs réussites et leurs défauts. Car tout ne fonctionne pas
toujours : le programme peut être incorrect, fragile, incomplet, ou faire ce qui est demandé de manière
très maladroite (par exemple jouer très mal aux échecs).

Derrière le spectacle, une question demeure : les langages de programmation vont-ils disparaître, ou
devenir au contraire encore plus importants pour préciser, contrôler et comprendre ce que l'IA produit ?

## Organisation des slides

Format cible : **60 min d'exposé + 30 min de questions**, ~230 étudiants (cœur IA ou coloration IA), le matin.

**Deux versions** :

- **Version courte (par défaut)** : `index.html` → `slides.md` — **80 slides d'exposé (~57 min)**
  suivies, après la slide Références, d'une section **Backup de 36 slides** (rien n'est perdu :
  protocole détaillé, tour de Babel SVG, anecdotes de bugs, figures supplémentaires…)
  à dégainer pendant les 30 min de discussion (touche `O` pour naviguer)
- **Version longue** : `long.html` → `slides-long.md` — **114 slides, ~81 min**,
  pour un créneau d'1h30 (les slides de backup y sont dans le fil principal)

Toute retouche de fond gagne à être faite dans les deux fichiers.

Le résumé ci-dessus est la slide 2 des deux versions ; elle est marquée `data-visibility="uncounted"`
pour ne pas décaler la numérotation utilisée dans `TIMELINE.md`, `chrono.html` et ce README.

## Lancer la présentation en local

```bash
cd PLs-AI-talk
python3 serve.py            # port 8000 par défaut
# version courte : http://localhost:8000
# version longue : http://localhost:8000/long.html
```

`serve.py` gère les requêtes « Range » (indispensables pour lire/rembobiner les vidéos —
`python3 -m http.server` ne les gère pas et spamme des `BrokenPipeError` inoffensifs).

reveal.js est vendorisé dans `reveal/` : **tout fonctionne hors ligne** (vidéos comprises).
La version en ligne est servie telle quelle par GitHub Pages depuis la branche `main`
(fichier `.nojekyll`). L'enregistrement vidéo de la séance (`semaine-ia-2026-live.mp4`, ~1 Go)
reste hors dépôt (`.gitignore`).

- `S` : vue présentateur (notes + chrono)
- `F` : plein écran, `O` : vue d'ensemble, `B` : écran noir
- Export PDF : ouvrir `http://localhost:8000/?print-pdf` puis imprimer en PDF depuis Chrome

## Fichiers

- `slides.md` — tout le contenu (séparateur de slide : `---`)
- `TIMELINE.md` — le minutage du jour J, bloc par bloc
- `chrono.html` — la même conduite avec un chronomètre (http://localhost:8000/chrono.html,
  à ouvrir sur un téléphone ou un second écran pendant l'exposé)
- `index.html` — configuration reveal.js
- `talk.css` — thème personnalisé : fond en dégradé, barres d'accent sous les titres,
  cartes (tableaux, bilans, citations), gros chiffres en dégradé doré, ombres sur les médias.
  Classes utiles : `.big`, `.cols`, `.ok`/`.ko`, `.findings`, `.smallest`, `.pixel`
  (rendu pixelisé assumé, pour les captures rétro type Doom COBOL), `.tallstrip`.
  Les slides de section ont des images de fond plein écran
  (`data-background-image` + `data-background-opacity` dans `slides.md`)
- `assets/img` — images (blogs, M&M's, Doom COBOL)
- `assets/videos` — captures bureau et mobile des jeux, `chatgpt-echecs.mp4`, `console.mp4`,
  `neveu.mp4`, `texcc-overleaf.mp4`. `fifacher-mobile-zoom.mp4` est la version recadrée de
  `fifacher-mobile.mp4` : la capture d'origine est un écran de téléphone en 360×640 dont seuls
  330×136 pixels portent du contenu, le reste est noir. Le recadrage plus un agrandissement
  lanczos ×3 donne 990×408, affiché au centre de la slide FIFAcher
- `assets/figs` — figures des papiers (Elo échecs, figures COBOL rendues depuis les PDF)

## Plan et minutage

Le minutage détaillé du jour J (repères `⏱ T+xx`, quoi couper si on déborde, slides de backup
par type de question, check-list du matin) est dans **`TIMELINE.md`**. Résumé — **60 min
d'exposé, 81 slides, puis 30 min de questions** :

| T+ | Section | Durée | Slides |
|----|---------|-------|--------|
| 0 | Titre + programme (avec la question de fond) | 2 min | 1–2 |
| 2 | 1. Programmer en français : démos, prompt, console, la bascule fin 2025 | 8 min | 3–14 |
| 10 | Le questionnement : le paradoxe, les compromis, les trois terrains | 5 min | 15–17 |
| 15 | 2. L'expérience polyglotte échecs | 10 min | 18–35 |
| 25 | 3. Langages ésotériques | 10 min | 36–49 |
| 35 | 4. COBOL | 10 min | 50–61 |
| 45 | 5. Synthèse : les mêmes lois, les oracles, le fossé, l'expertise | 5 min | 62–67 |
| 50 | 6. Et maintenant ? Trois hypothèses, enseigner, la réponse | 8 min | 68–78 |
| 58 | Pour conclure (mosaïque) + Merci + Références | 2 min | 79–81 |
| 60 | Questions, avec les 36 slides de backup en réserve | 30 min | 82–118 |

La version longue (`long.html`) suit la même structure avec les slides de détail dans le fil (115 slides, ~81 min).

## Sources

- https://blog.mathieuacher.com/CallOfAcherFIFAcherJeuxIA/
- https://blog.mathieuacher.com/BFChessChessEngineBrainfuck/
- https://blog.mathieuacher.com/CodingAgentsMnMLang/
- https://blog.mathieuacher.com/TeXCCChessEngine/ (TeXCCChess ; vidéos : https://youtu.be/ngHMozcyfeY Overleaf, https://youtu.be/Tg4r_bu0ANY local)
- https://blog.mathieuacher.com/PL-ultimate-llm/ (PL Catalog — SWH & CodeCommons)
- https://arxiv.org/abs/2606.13763 (Acher & Jézéquel, moteurs d'échecs polyglottes)
- Papier COBOL : `../cobol-meta-analysis/draft/paper.pdf` (Acher, Kebaili, Khelladi, Espinasse).
  Le « compresseur livré 100 % en C, exclu du corpus » (slide évasion COBOL) y figure : section corpus
  (« One compression attempt (cobol-compress-cc) was excluded because its deliverable is C, not COBOL »),
  paragraphe « COBPACK C-first vs COBOL-first » (RQ1, 1 123 LoC de C) et section « evasion »
- https://github.com/acherm/agentic-arnoldc (triple interpréteur ArnoldC → MnM → Brainfuck)
- « ChatGPT rêve-t-il de cavaliers électriques ? » — Monsieur Phi, https://www.youtube.com/watch?v=6D1XIbkm4JE (mentionnée slide 21)
- « Who Codes When AI Can Generate Code? Impacts of Generative AI on Professional Developers, End Users,
  and Researchers », exposé de Mathieu Acher au séminaire SOTELO « De l'impact de l'IA-générative sur le
  génie logiciel », 4 juin 2025 — vidéo : https://www.youtube.com/watch?v=Aj5arTQzMQ4&t=822s
  (repris slide « Et il n'y a pas UN contexte, mais mille » et dans les Références)

## À vérifier / personnaliser avant le jour J

- [x] Slide titre : date et événement en place (vendredi 4 septembre 2026, Semaine de l'IA, Université de Rennes)
- [x] Console Claude Code : vidéo intégrée (0902.mov + capture, fondu 1 s, sans le son) —
      préparer la démo live si prévue, la slide sert de filet de sécurité
- [x] Vidéo du neveu : intégrée (« 0902 (1).mov » converti en `assets/videos/neveu.mp4`)
- [x] Vidéo TeXCCChess/Overleaf : intégrée (`texcc-overleaf.mp4`, 640×360 — résolution
      maximale disponible sur YouTube)
- [x] ASHFALL et FIFAcher : remplacés par les captures bureau 2560×1440 du 03/08
      (recadrées sans la barre du navigateur, 1600px H.264)
- [ ] Démo live éventuelle : les jeux sont jouables sur https://blog.mathieuacher.com/ashfall/
      et /fifacher/ (prévoir le réseau, sinon les vidéos font le travail)
- [x] Chiffres COBOL recoupés entre slides : les deux compilateurs font 11 680 et 15 912 lignes,
      donc « 27 000+ lignes » sur la slide « Le résultat le plus fou » (c'était « 13 000+ »)
- [x] Relecture finale du 3 septembre : 7 débordements corrigés (slides 7, 10, 45, 76, 81, 92, 98),
      programme Brainfuck de la slide 94 complété (il affichait « Hello World » sans le « ! »),
      ~520 Elo réattribués aux portages Rust/COBOL et non à Java→COBOL, accords et notes corrigés
