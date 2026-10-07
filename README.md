# 16:9 Dark Beamer Template for the University of Sussex

An unofficial LaTeX Beamer theme in the University of Sussex brand identity (per the [University of Sussex Identity Guidelines](https://www.sussex.ac.uk/webteam/gateway/file.php?name=uos-11932---logo-and-updated-guidelines-ac6.pdf&site=514) V.2, February 2026). 

See [sussex.pdf](sussex.pdf) for the compiled demo.

> **Not an official University of Sussex template.** For official templates and master logo artwork, contact brand@sussex.ac.uk.

## Quick start

1. Clone or download this folder.
2. Edit `sussex.tex`, or start a new file with:

   ```latex
   \documentclass[11pt,t,aspectratio=169]{beamer}
   \usetheme{sussexdark}
   \title{My talk}
   \author{Your Name}
   \institute{University of Sussex}
   \titlegraphic{\includegraphics[height=0.95in]{logos/sussex-logo-chalk.pdf}}
   ```

3. Compile with `pdflatex` (or `latexmk -pdf sussex.tex`).

To use the theme from any folder, copy the `.sty` files and the `logos/` folder into your TeX tree. On macOS that is `~/Library/texmf/tex/latex/sussexdark/`. On Linux, add the folder to `TEXINPUTS`, e.g. `export TEXINPUTS=${HOME}/LaTeX//:${TEXINPUTS}`.

## Files

| File | Purpose |
|------|---------|
| `beamerthemesussexdark.sty` | Main theme: loads the four parts below |
| `beamercolorthemesussexdark.sty` | Full Sussex palette and colour assignments |
| `beamerfontthemesussexdark.sty` | Libre Baskerville titles, Inter body text |
| `beamerinnerthemesussexdark.sty` | Title page, backgrounds, section page |
| `beamerouterthemesussexdark.sty` | Footer with author, section, page number and logo |
| `logos/` | Vector logos (primary and secondary, chalk and green) |
| `sussex.tex` | Demo deck |

## Options

- `\usetheme[footlogo=false]{sussexdark}` hides the small logo in the footer.
- `\usetheme[shadow]{sussexdark}` adds shadows to blocks.
- `\renewcommand{\sussexfootlogo}{\includegraphics[height=2.2ex]{...}}` swaps the footer logo.
- The `\AtBeginSection` block in `sussex.tex` produces the green section slides. 

## Logos

| File | Use on |
|------|--------|
| `logos/sussex-logo-chalk.pdf` | Green backgrounds (title slide) |
| `logos/sussex-logo-green.pdf` | Chalk backgrounds |
| `logos/sussex-logo-secondary-chalk.pdf` | Green, where space is tight (footer) |
| `logos/sussex-logo-secondary-green.pdf` | Chalk, where space is tight |

Per the guidelines, keep clear space around the logo (twice the height of the "Y" in the wordmark). 

## Colours

Every colour from the guidelines is defined, so you can use `\color{usturquoise}`, `\cellcolor{usshellpeach}` and so on.

| Palette | Macros |
|---------|--------|
| Sussex by the Sea | `usgreen` #033803, `uschalk` #EAE5DD, `usturquoise` #32D8C5 (each with official tints `…80`, `…60`, `…40`, `…20`) |
| Brighton | `usargusred`, `usnorthlaineorange`, `uscarouselyellow`, `usrockpink`, `uspavilionpurple`, `usalbionblue`, `usbeachhutblue`, `usstanmergreen` |
| South Downs | `usshellpeach`, `usheatherpurple`, `usrampionlilac`, `usflintgrey`, `usoceanteal`, `usadonisblue`, `usditchlinggreen`, `usdownlandgreen` |

## Fonts

The theme uses Libre Baskerville for titles and Inter for body text, with Inter SemiBold in the footer. Both come with TeX Live and MiKTeX. Code uses Latin Modern Typewriter. If you'd rather use `minted` for code, it still works, but needs `-shell-escape` and Python's Pygments.

## Credits

Adapted from the [16:9 Dark Beamer Template by Guanyang Xue](https://www.overleaf.com/latex/templates/my-dark-beamer-template-for-lehigh-university/jgwzhmcgvxnh), which was modified from Alex Pacheco's original. Colours, typefaces and logos follow the University of Sussex Identity Guidelines V.2 (February 2026).
