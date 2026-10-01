# Heilbronn configurations

The [Heilbronn triangle problem](https://en.wikipedia.org/wiki/Heilbronn_triangle_problem) is to place n points in a unit-area region such that the smallest triangle determined by any three points achieves the largest possible area A(n).

This project documents configurations that I have found or refined that improve on published best-known coordinate values.

The entries give exactly verified feasible lower bounds for the published coordinate literals. They do not claim optimality unless noted.

## Square container

Point configurations in the unit square

| Points | Record period | Verified lower bound | History / files |
|---|---|---|---|
| 23 | 2026-09-25 – current | 0.009757289713314772257160702006 | [History](squares/square-n23/README.md) · [Coordinates](squares/square-n23/2026-09-29-0.009757289713314772257160702006/coordinates.txt) · [SVG](squares/square-n23/2026-09-29-0.009757289713314772257160702006/configuration.svg) · [PNG](squares/square-n23/2026-09-29-0.009757289713314772257160702006/configuration.png) |
| 19 | 2026-09-26 – current | 0.013947862081484501285699980568 | [History](squares/square-n19/README.md) · [Coordinates](squares/square-n19/2026-09-26-0.013947862081484501285699980568/coordinates.txt) · [SVG](squares/square-n19/2026-09-26-0.013947862081484501285699980568/configuration.svg) · [PNG](squares/square-n19/2026-09-26-0.013947862081484501285699980568/configuration.png) |
| 25 | 2026-09-26 – current | 0.008230069426525093386004329217 | [History](squares/square-n25/README.md) · [Coordinates](squares/square-n25/2026-09-26-0.008230069426525093386004329217/coordinates.txt) · [SVG](squares/square-n25/2026-09-26-0.008230069426525093386004329217/configuration.svg) · [PNG](squares/square-n25/2026-09-26-0.008230069426525093386004329217/configuration.png) |
| 35 | 2026-09-24 – current | 0.004432287444307324185873611323 | [History](squares/square-n35/README.md) · [Coordinates](squares/square-n35/2026-09-26-0.004432287444307324185873611323/coordinates.txt) · [SVG](squares/square-n35/2026-09-26-0.004432287444307324185873611323/configuration.svg) · [PNG](squares/square-n35/2026-09-26-0.004432287444307324185873611323/configuration.png) |
| 21 | 2026-09-24 – current | 0.011473760785701210268349183177 | [History](squares/square-n21/README.md) · [Coordinates](squares/square-n21/2026-09-26-0.011473760785701210268349183177/coordinates.txt) · [SVG](squares/square-n21/2026-09-26-0.011473760785701210268349183177/configuration.svg) · [PNG](squares/square-n21/2026-09-26-0.011473760785701210268349183177/configuration.png) |

## Triangle container

Point configurations in a triangle. Coordinates use the unit right triangle (`x >= 0`, `y >= 0`, `x + y <= 1`); lower bounds are minimum triangle area divided by container area. The figures show the equivalent configuration in an equilateral triangle.

| Points | Record period | Verified lower bound | History / files |
|---|---|---|---|
| 20 | 2026-09-30 – current | 0.012609391528641322601846401770 | [History](triangles/triangle-n20/README.md) · [Coordinates](triangles/triangle-n20/2026-10-01-0.012609391528641322601846401770/coordinates.txt) · [SVG](triangles/triangle-n20/2026-10-01-0.012609391528641322601846401770/configuration.svg) · [PNG](triangles/triangle-n20/2026-10-01-0.012609391528641322601846401770/configuration.png) |

Record period continues across improvements of our own result; individual result dates, gains and earlier periods remain in each history.

Periods refer to documented best-known coordinate bounds, not construction priority; `current` reflects reviewed evidence, not live monitoring. Historical comparisons retain their stated baselines. See also [Tej Stead's catalogue](https://github.com/tejstead/heilbronn-site).

## Further detail

Current versions preserve every stored digit of the verified source coordinates: 60 decimal places for square n=19, 21, 23 and 25, and 160 decimal places for square n=35 and triangle n=20. Feasibility and every triangle have been checked using exact rational arithmetic on those published literals. Full precision means the stored numerical configuration, not a claim of exact optimal coordinates.
The lower bounds above are computed from the published coordinates and conservatively truncated to 30 decimal places for display; the coordinate files retain their full precision.

Versions are named `YYYY-MM-DD-<lower-bound>`; the date is the export date. Improved configurations receive new version folders, retaining earlier discoveries in the configuration history. Restoring omitted coordinate digits is not a new discovery and does not change its discovery date.

Each version contains `coordinates.txt`, `meta.json`, `configuration.svg` and `configuration.png`. Separate 30-place coordinate files, truncated toward zero and independently verified, are prepared for [Tej Stead submissions](https://github.com/tejstead/heilbronn-site/blob/main/CONTRIBUTING.md). Their achieved scores can differ from the full-precision values in this repository.

The figures are generated directly from that version's published coordinates. They show the points and highlight triangles whose areas are within a relative tolerance of `1e-9` of the minimum. This tolerance affects the illustration only; the reported lower bound is verified exactly. The SVG preserves the coordinate literals in point tooltips and supports selection when opened in a scripting-enabled SVG viewer. The PNG is a static rendering of the same figure; embedded SVG previews may also be static.

For a catalogue of best known configurations across all `n` see [Tej Stead's Heilbronn site](https://math.tejstead.com/heilbronn/)

## Method

Configurations have been found through a local solver employing various optimisation techniques. OpenAI's ChatGPT and Codex have been used to help develop and test the solver.

## Licence and citation

The coordinate data, written content and SVG/PNG illustrations in this repository are licensed under the [Creative Commons Attribution 4.0 International licence](LICENSE). To cite the collection, use the metadata in [`CITATION.cff`](CITATION.cff).
