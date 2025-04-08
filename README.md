## ⚠️ Deprecated

This project is no longer actively maintained.

It is recommended to use [NeoStandard](https://github.com/neostandard/neostandard) instead. NeoStandard offers a modern approach to JavaScript linting, compatible with ESLint's flat config and built for today's ecosystem.

To migrate, you can follow these steps:

```bash
# 1. Uninstall healthier
npm uninstall healthier

# 2. Install NeoStandard and ESLint
npm install -D neostandard eslint

# 3. Generate an ESLint flat configuration file (eslint.config.js)
#    Use --esm for ESM projects or omit for CJS projects
npx neostandard --esm > eslint.config.js

# 4. Run ESLint
eslint . # Or specify your source files/directories
```

NeoStandard provides a similar zero-config experience but leverages the latest ESLint features and community best practices.

# eslint-plugin-healthier

Eslint plugin for https://github.com/KidkArolis/healthier and https://github.com/KidkArolis/eslint-config-healthier. Healthier is an opinionated linter that only applies non code style related linting rules, which makes it a great companion for code formatters such as Prettier.

## Usage

Because npm and yarn flattens dependencies, you actually, technically, don't need to install this plugin and can only install eslint-config-healthier. This is to make using this eslint config more convenient. This will be improved when eslint makes it possible for configs to depend on plugins.

    npm i -D eslint-plugin-healthier

## Rule prefix

Healthier plugin depends on the following plugins to expose these to eslint-config-healthier:

- eslint-plugin-standard
- eslint-plugin-node
- eslint-plugin-import
- eslint-plugin-promise
- eslint-plugin-react

By reexporting these plugins, eslint forces us to change the prefix for all those rules to `healthier/`. This will be improved when eslint makes it possible for configs to depend on plugins.
