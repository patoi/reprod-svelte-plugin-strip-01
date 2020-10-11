# Reproducing Svelte Plugin Strip error

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

## Add next lines for testing purpose

`App.svelte`, code block strip:

```javascript
unittest: {
  name = 'Strip doesn\'t work'
}
```

`rollup.conf.js`:

```javascript
import strip from '@rollup/plugin-strip';
...

strip({
  labels: ['unittest']
}),
```

## Run commands

`npm install`

`npm run dev`

## Checking

Visit http://localhost:5000

You see this one, if strip plugin doesn't work: `HELLO STRIP DOESN'T WORK!`

**Expected behaviour:**

You see this one: `HELLO WORLD!`

