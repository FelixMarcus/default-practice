# Local Development

## Automated setup

It should be possible to configure any new workstation with an easy to run, comprehensive and automated script to provide all required functionality and quality of life improvements without having to chase them or tinker. We want to be able to run a command, wait a short time, and then start moving at full speed.

For MacOSX machines, [I maintain my own](https://github.com/FelixMarcus/mac-setup)

## Pre-commit hooks

Every repo should automatically run git hooks to formulate and check changes before they are committed or pushed.

Typically I prefer [Lefthook](https://github.com/evilmartians/lefthook) - it provides a rich set of options, storable in code with a rich console output. It should be installed locally within the repo (not globally - [see Ways of Workings](./wow.md#LocalDependencies)).

Lefthook is also available for most modern languages frameworks. For Example, Lefthook can be installed on npm thus:

```
npm i Lefthook --save-dev
npx lefthook install
```

This will sync the necesary git hooks for lefthook to run. If `lefthook install` is added as a postinstall script in the package.json file, e.g.:

```json
{
  "scripts": {
    "postinstall": "lefthook install" 
  }
}
```

Then the hooks will be automatically created anytime the repo is downloaded and installed - useful for creating consistency across multiple environments.
