# Distinctive Asset Grid

Is that logo, colour or sound actually yours? Paste the results of an unbranded asset test and get each asset's fame, uniqueness, a 0 to 100 distinctiveness score with a range, and which of the four grid boxes it sits in, with a chart.

Open `index.html` in any browser. No build step, no dependencies, no network calls. Your data stays in your browser.

- **Input:** a CSV with `asset,respondents,brand`, then one column per rival. An optional `prompted` column flags tests where people saw a brand list. The pre-filled rows are invented, to show the format.
- **Measures:** fame (named you / saw the asset), uniqueness (named you / named any brand), and a score of 100 x fame^w x uniqueness^(1 - w), with w = 0.5 by default.
- **Boxes:** use or lose, invest, avoid solo use, and test or ignore, with how sure the data is of the box.
- **Also shows:** a fame by uniqueness chart with 95% ranges, a table of every asset, who gets the credit when an asset leaks, warnings for thin samples and prompted tests, and a sample-size helper.
- **Share:** a paper-ground PNG card.

A browser version of the scoring in [assetscan](https://github.com/ben-j-ads/assetscan). Fame, uniqueness, score, box and the Wilson ranges match it exactly. The score range and box probabilities come from 4,000 seeded Dirichlet draws and can differ from the Python app's by about a point. assetscan also handles segments and an execution audit.

It scores the data you collect and does not run the survey: use unbranded stimuli, category buyers and unprompted recall (Romaniuk, *Building Distinctive Brand Assets*, 2018). The lines (fame 30%, uniqueness 50%) and the bands (20, 45, 70) are conventions, not published standards, and the score has not been tested against sales. Pairs with cover-the-logo, which makes the stimuli.

## License

Code is MIT licensed ([LICENSE](LICENSE)). The bundled fonts (Bricolage Grotesque, Archivo) are SIL OFL 1.1, with licenses in `fonts/`. The ben.j.ads wordmark and footnote mark in `logo/` are Ben Johnston's brand assets and are not covered by the MIT license.
