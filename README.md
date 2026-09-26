# Heilbronn configurations

The [Heilbronn triangle problem](https://en.wikipedia.org/wiki/Heilbronn_triangle_problem) is to place n points in a unit-area region such that the smallest triangle determined by any three points achieves the largest possible area A(n).

This project documents configurations that I have found that beat published best known results.

The entries give exactly verified feasible lower bounds for the displayed coordinate literals. They do not claim optimality unless noted.

## Square container

Point configurations in the unit square

| Points | Previous best known | New result | Improvement | Record since | Record until | Data |
|---|---|---|---|---|---|---|
| 21 | 0.011265852716080434775405475359 | 0.011473760785701210268349183177 | 1.8455% | 2026-09-24 | current | [Coordinates](squares/square-n21/2026-09-26-0.011473760785701210268349183177/coordinates.txt) · [Metadata](squares/square-n21/2026-09-26-0.011473760785701210268349183177/meta.json) · [SVG](squares/square-n21/2026-09-26-0.011473760785701210268349183177/configuration.svg) · [PNG](squares/square-n21/2026-09-26-0.011473760785701210268349183177/configuration.png) |
| 23 | 0.009457434268315443447496308853 | 0.009643319809002482004777880110 | 1.9655% | 2026-09-25 | current | [Coordinates](squares/square-n23/2026-09-26-0.009643319809002482004777880110/coordinates.txt) · [Metadata](squares/square-n23/2026-09-26-0.009643319809002482004777880110/meta.json) · [SVG](squares/square-n23/2026-09-26-0.009643319809002482004777880110/configuration.svg) · [PNG](squares/square-n23/2026-09-26-0.009643319809002482004777880110/configuration.png) |
| 25 | 0.007933175183761128423551968736 | 0.008230069426525093386004329216 | 3.7424% | 2026-09-26 | current | [Coordinates](squares/square-n25/2026-09-26-0.008230069426525093386004329216/coordinates.txt) · [Metadata](squares/square-n25/2026-09-26-0.008230069426525093386004329216/meta.json) · [SVG](squares/square-n25/2026-09-26-0.008230069426525093386004329216/configuration.svg) · [PNG](squares/square-n25/2026-09-26-0.008230069426525093386004329216/configuration.png) |
| 35 | 0.004409104135564505128660709183 | 0.004427409706281408864560795080 | 0.4152% | 2026-09-24 | current | [Coordinates](squares/square-n35/2026-09-26-0.004427409706281408864560795080/coordinates.txt) · [Metadata](squares/square-n35/2026-09-26-0.004427409706281408864560795080/meta.json) · [SVG](squares/square-n35/2026-09-26-0.004427409706281408864560795080/configuration.svg) · [PNG](squares/square-n35/2026-09-26-0.004427409706281408864560795080/configuration.png) |

Record since is the discovery date of the configuration.

Previous bests: [Tej Stead's catalogue, 26 September 2026](https://github.com/tejstead/heilbronn-site/tree/dfff099b34d6ea7ace1ea078aadc21f13a2d5264/data/canonical/square). Percentage improvements are calculated from the exact coordinate values.

## Further detail

Published coordinates have 30 decimal places, truncated toward zero. Feasibility and every triangle have been checked using exact rational arithmetic on those published literals.
The lower bounds above are computed from these exported coordinates and truncated to 30 decimal places.

Versions are named `YYYY-MM-DD-<lower-bound>`; the date is the export date. Future improvements receive new version folders.

Each version contains `coordinates.txt` and `meta.json` in this [submission format](https://github.com/tejstead/heilbronn-site/blob/main/CONTRIBUTING.md), together with `configuration.svg` and `configuration.png`.

The figures are generated directly from that version's published coordinates. They show the points and highlight triangles whose areas are within a relative tolerance of `1e-9` of the minimum. This tolerance affects the illustration only; the reported lower bound is verified exactly. The SVG preserves the coordinate literals in point tooltips and supports selection when opened in a scripting-enabled SVG viewer. The PNG is a static rendering of the same figure; embedded SVG previews may also be static.

For a catalogue of best known configurations across all `n` see [Tej Stead's Heilbronn site](https://math.tejstead.com/heilbronn/)

## Method

Configurations have been found through a local solver employing various optimisation techniques. OpenAI's ChatGPT and Codex have been used to help develop and test the solver.

## Licence and citation

The coordinate data, written content and SVG/PNG illustrations in this repository are licensed under the [Creative Commons Attribution 4.0 International licence](LICENSE). To cite the collection, use the metadata in [`CITATION.cff`](CITATION.cff).
