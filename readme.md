## Vue-Component-Starter

> A template to help you create vue3.x component

You can create yourself component quickly with it.

## Feature

- ⚡️ serve and build based on [vite](https://github.com/vitejs/vite)
- ✨ format with [pretty-quick](https://github.com/azz/pretty-quick)
- 🤙🏻 eslint support
- ⚙️ Unit Testing with [Vitest](https://github.com/vitest-dev/vitest)
- 🦾 TypeScript, of course
- 🎈 release package easily with [np](https://github.com/sindresorhus/np)

## Try it now!

> vue-component-starter require Node >=14

### Github Template

[Create repo from this template on Github](https://github.com/peterroe/vue-component-starter/generate)

### Clone to local

```shell
$ npx degit peterroe/vue-component-starter myComponent
$ cd myComponent
$ pnpm i
```

Don't forget initialize `.git` if you choose to clone locally:

```shell
$ git init
```

## Development

Just run and visit <http://localhost:3000>

```shell
$ pnpm dev
```

## Build

To build the Component, run:

```shell
$ pnpm build
```

And you will see the generated fie in `dist` that ready to be served.

## Publish your component

> Before you publish your component, you must give your component a new name in order to prevent conflicts with other people's component names.

Update `package.json`, and take a unique `name` for your `npm package`:

```diff
{
- "name": "vue-component-starter"
+ "name": "your-component-name"
}
```

You better also update the registered component name in `src/index.ts`:

```diff
export function install(app: App) {
- app.component('MyComponent', MyComponent)
+ app.component('yourComponentName', MyComponent)
}
```

Run `pnpm build` again to get the right files.

Make sure your are logged into [npm](https://www.npmjs.com/), and run:

```shell
$ pnpm release
```

For more details about publish, please check [np](https://github.com/sindresorhus/np).
