# Boilerplate Static Analysis

## Instructions
Run `npm install`.
Try add some errors, weird spacing, etc. and then run `validate`, or try commit with errors. The CLI output should stop and show you what's wrong. If your code passes, it will auto-format & auto-lint your /src files, and build.

## Linting
Linting is done with `eslint`. The package is extended in `.eslintrc` to include good presets, cover typescript errors and avoid conflicts with Prettier.

## Formatting
Formatting is done with `prettier`, with config set in `.prettierrc`. If you have a the editor extension, you can enable format on save and it should use this config over the editor's.

## Type Checking
`typescript` is used only type checking. Compiling is done by Babel, hence `"noEmit": true,` in the tsconfig.json.

With the presets set for the above, there is a `validate` script that will run and check all the above. You can run this at any time during development to find errors.

## Automation
`lint-staged` is used to run linting and formatting when committing.
`husky` is used to runcheck types, run linting and formatting, and build pre-commit, so nothing broken/unformatted is ever committed.