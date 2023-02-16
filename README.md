[![NPM](https://img.shields.io/npm/v/@sargunv/typescript-config)](https://www.npmjs.com/package/@sargunv/typescript-config)

# @sargunv/typescript-config

My personal Typescript configs.

## Usage

### Generic projects:

The basic preset configures all my preferences for type checking behavior, but
is agnostic to environment. It'll need additional configuration for `module`,
`moduleResolution`, `lib`, and `target` depending on the project. It also
defaults to `noEmit: true`.

In tsconfig.json:

```json
{
  "extends": "@sargunv/typescript-config"
}
```

### Node projects:

This preset extends the generic preset for a modern Node environment.

In tsconfig.json:

```json
{
  "extends": "@sargunv/typescript-config/presets/node",
  "include": ["src/**/*"],
  "compilerOptions": {
    "rootDir": "src",
    "outDir": "dist"
  }
}
```

If using CommonJS instead of ESM, extend `node-cjs` instead of `node`.
