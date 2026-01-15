# Strapi 5 Starter

This starter repository facilitates the creation of new Strapi projects using the configuration described below.

To learn how to use a GitHub template repository, check
out [Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

![project status](https://img.shields.io/badge/project_status-active-success?style=for-the-badge)

## Tech Stack

### Backend

- **Headless CMS**: [Strapi 5](https://strapi.io/)

## Initial Setup

To regenerate the `.env` file and initial config values for the `strapi` field in `package.json`, you can run the command below. This will quickly scaffold a new Strapi project ignored by Git and with the same options as this starter.

```bash
# The `echo` command will accept the default value for the first prompt (anonymous A/B testing: no)
echo | npx create-strapi-app@latest strapi-skeleton --skip-cloud --dbclient sqlite --dbfile .tmp/data.db --no-example --typescript --no-install --no-git-init
cp strapi-skeleton/.env .env
# Manual steps:
# - Copy the `strapi` field values from `strapi-skeleton/package.json` to this repo's `package.json`
# - Remove the temporary folder: `git clean -fx strapi-skeleton`
# - Update environment variables as needed.
```

## How to Update

```bash
npm run upgrade # Update Strapi dependencies
npm install --save-exact --save-dev prettier@latest
```

## Notes

- The GitHub Action `actions/setup-node@v6` relies on both `package.json` `engines` and `devEngines` to set the Node.js version and automatically cache npm dependencies.

## Dev Environment & Tools

- **System**: [Ubuntu](https://ubuntu.com/desktop)
- **Editor**: [VS Code](https://code.visualstudio.com/)
- **Formatter**: [Prettier](https://prettier.io/)
- **AI assistant**: [GitHub Copilot](https://github.com/features/copilot)

## Copyright

© 2026 Johnny Gérard
