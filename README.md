# mhowat1.github.io

Personal site, including coursework for PP434 Automated Data Visualizations.
Plain HTML and CSS served by GitHub Pages, so no Jekyll or build step is needed.

## Structure

```
index.html            Landing page: intro + "Selected work" cards
portfolio.html        PP434 Class Projects (CC01, CC02 charts)
class-portfolio.html  PP434 Class Portfolio (weekly exercise charts)
research.html         Publications & Current Projects tab (placeholder content)
about.html            About, education, experience, skills
assets/style.css      All styling (edit the variables at the top)
images/               portrait.jpg and project thumbnails
*.json, *.csv         Vega-Lite chart specs and data used by the PP434 pages
```

## To do

1. Replace `your-profile` with your LinkedIn handle.
2. Add `images/portrait.jpg` (square works best).
3. Fill in `research.html` and `about.html`.

Preview locally with `python3 -m http.server` in this folder and visit http://localhost:8000
(the charts load their JSON specs, so opening the files directly may not show them).

## Adding a chart to a PP434 page

Copy a `<section class="chart-section">` block, give its `<figure>` a new id (e.g. `Location5`),
and add a matching `vegaEmbed('#Location5', "your_chart.json");` line in the script at the bottom.

## Adding a project card

Copy a `<a class="card">` block on `index.html`. To show a thumbnail, replace
`<div class="thumb">Image</div>` with `<img class="thumb" src="images/your-image.png" alt="Short description">`.
A `card soon` block is a dashed, non-clickable placeholder.
