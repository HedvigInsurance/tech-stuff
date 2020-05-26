# Contributing to web projects @ Hedvig

Regarding tech, this is good to know when developing web at Hedvig:

  - Currently we're quite invested in React and would like to keep our tech stack as streamlined as possible, but
    we're still open to and experiment with new tech. As per our tech values, we're not afraid to
    experiment with new things but we like battle-tested technologies when possible.
  - We're picky about code style, tests and types - which means:
    - We use TypeScript
    - We use [Prettier](https://www.npmjs.com/package/prettier) and linting (eslint/tslint)
    - As long as we invest in React we prefer Jest for testing
    - We use CI to enforce these constraints (which also means that tests, linting and type
      checks should pass before mergeing a PR). So before opening a PR, remember the 3 checks :)
  - We prefer [Yarn](https://yarnpkg.com/) for package management
  - We prefer [Storybook](https://storybook.js.org/) for building standalone and reusable components

## Getting your machine ready for web development

Although many use Intellij or WebStorm as editors we aim to have editor agnostic environments
but there are some things you'll need to keep in mind when setting up your machine for web development.

  - Install Node.js via [NVM](https://github.com/nvm-sh/nvm#installing-and-updating) - in this way you can jump
    between Node versions without too much pain. We can't always guarantee to have the same node version requirements
    for all projects.
  - Install [yarn](https://yarnpkg.com/) via NPM (by using `npm install -g yarn`)

After having done these installs you should be able to use all web projects with ie `yarn watch` for starting a development
server, `yarn typecheck` for - well - type checking, `yarn lint` for linting, `yarn test` for testing and so on.
Check your project's `package.json` for details on which scripts your specific project supports.


## RFCs (request for change - contributing to web projects)

Like the rest of tech @ Hedvig we work exclusively with code review and pull requests. The exception might be making very minor
changes like white-listing a single domain in your project's CSP or similar. When making a PR, make sure to assign the
[`@HedvigInsurance/www`](https://github.com/orgs/HedvigInsurance/teams/www) team to it, and get signoff someone from
that team before merging. If your change is visual feel free to provide a screenshot/screen recording of your change
so it's more easy to understand what to expect from the code.

