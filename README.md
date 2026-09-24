# scenariolab.org

Static site for [scenariolab.org](https://scenariolab.org), hosted on GitHub Pages. (ECHO 2026-09-23)

- `index.html` – landing page for Scenario Lab, with Europe 2032 as the featured scenario.
- `europe-2032/index.html` – the Europe 2032 reader. Generated, do not edit by hand.
- `CNAME` – custom domain for GitHub Pages.

## Rebuilding Europe 2032

The reader is built from the story files in the Scenario Lab repo:

```bash
cd "../Scenario Lab 3"
python3 scripts/build_story.py scenarios/europe-2032 --standalone \
    --out ../scenariolab.org/europe-2032/index.html
```

Then commit and push here. GitHub Pages deploys on push.

(ECHO 2026-09-24) The footer's "Updated" date is the latest commit in Scenario Lab that changed the story's content, linked to that commit on GitHub. Commit and push Scenario Lab before building, or the link points to a commit GitHub does not have yet; the build warns when story files are uncommitted.

## DNS

The domain is registered at Inleed. The apex points to GitHub Pages:

- A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `www` CNAME: `itangalo.github.io`

