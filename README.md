
# @ktsierra/prettier-config

My personal Prettier configuration for consistent code formatting across projects.

## Installation

```bash
npm install -D @ktsierra/prettier-config prettier
```

## Usage

To use this shared configuration in your project, create a \`prettier.config.js\` (or \`prettier.config.cjs\`) file at the root of your repository:

### For ESM (\`.js\`)

```js
import config from '@ktsierra/prettier-config';

export default config;
```

### For CommonJS (\`.cjs\`)

```js
module.exports = require('@ktsierra/prettier-config');
```

## What's Included

- No semicolons (\`semi: false\`)
- Single quotes (\`singleQuote: true\`)
- 2-space indentation (\`tabWidth: 2\`)
- Trailing commas where valid in ES5 (\`trailingComma: 'es5'\`)
- Bracket spacing enabled (\`bracketSpacing: true\`)
- Brackets on new lines for JSX (\`bracketSameLine: false\`)
- Line width set to 80 characters (\`printWidth: 120\`)

## Example Configuration

```js
/** @type {import("prettier").Config} */
export default {
  semi: false,
  singleQuote: true,
  tabWidth: 2,
  trailingComma: 'es5',
  bracketSpacing: true,
  bracketSameLine: false,
  printWidth: 120,
};
```

## Extending or Overriding

If you want to customize the configuration further, you can extend it in your own \`prettier.config.js\`:

```js
import baseConfig from '@ktsierra/prettier-config';

export default {
  ...baseConfig,
  // Your custom overrides
  printWidth: 100,
};
```

## Why Use This?

- **Consistency:** Enforces the same formatting rules across all your projects.
- **Simplicity:** One shared config, easy to update and maintain.
- **Editor/CI Friendly:** Works seamlessly with editors (like Neovim with prettierd) and CI pipelines.

## Requirements

- [Prettier](https://prettier.io/) (added as a peer dependency)
- Node.js 14 or newer

Feel free to open issues or PRs if you want to suggest improvements!
