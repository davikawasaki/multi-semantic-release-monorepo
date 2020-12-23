# Monorepo Management Release using Multi Semantic Releases

Management release for monorepo using multi semantic releases

## Startup steps

```
$ npm init
$ npm i -D lerna husky commitizen git-cz @commitlint/{config-conventional,cli,prompt} semantic-release @qiwi/multi-semantic-release @semantic-release/{npm,git,github,commit-analyzer,release-notes-generator}
$ npx lerna init --independent
$ mkdir packages/app packages/lib
$ npx lerna create app
$ npx lerna create lib
$ npx lerna add lib --scope=app
$ echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

## References

https://github.com/dhoulb/multi-semantic-release

https://github.com/lerna/lerna/tree/main/commands/version

https://samhogy.co.uk/2018/08/lerna-independent-mode-with-semver.html

https://kevinkreuzer.medium.com/the-way-to-fully-automated-releases-in-open-source-projects-44c015f38fd6

https://commitlint.js.org/#/?id=getting-started

https://www.conventionalcommits.org/en/v1.0.0/
