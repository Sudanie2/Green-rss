# Green RSS Feed

This repository hosts a generated `rss.xml` file for the "Kosodate Green" project. The feed is built automatically from the upstream `news.json` file.

## Automated generation

A GitHub Actions workflow runs daily (`cron: "10 1 * * *"`, which is 10:10 JST) to fetch the JSON, convert it to RSS, and commit any changes. The workflow also ensures a `.nojekyll` file is present so GitHub Pages serves the XML correctly. Adjust the cron schedule in `.github/workflows/rss-generator.yml` if needed.

### Triggering the workflow manually

To regenerate the feed outside the schedule, open the **Actions** tab, select **Generate RSS Feed**, and click **Run workflow**. This uses the `workflow_dispatch` trigger.

## Contributing

Changes to the feed should come from updates to the workflow or the source JSON, not manual edits to `rss.xml`. Please submit pull requests for any modifications and keep commit messages clear.
