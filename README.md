# clerk-astro-error

### Setup

Add `.env` file with

```
PUBLIC_CLERK_PUBLISHABLE_KEY=...
CLERK_SECRET_KEY=...
```

Run `yarn`

Run `yarn dev`

Shows following error in browser:

```
TypeError
An error occurred.

Astro2.locals.auth is not a function
```

```
control/SignedOutSSR.astro:2:33
---
const { userId } = Astro.locals.auth();
^
---

{!userId ? <slot /> : null}
```

```
TypeError: Astro2.locals.auth is not a function
    at ~/code/clerk-astro-error/node_modules/@clerk/astro/components/control/SignedOutSSR.astro:2:33
    at AstroComponentInstance.SignedOutSSR [as factory] (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/astro-component.js:16:12)
    at AstroComponentInstance.init (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/astro/instance.js:34:29)
    at AstroComponentInstance.render (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/astro/instance.js:44:30)
    at Object.render (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/component.js:355:23)
    at renderChild (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/any.js:33:18)
    at ~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/astro/render-template.js:30:29
    at new BufferedRenderer (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/util.js:129:26)
    at createBufferedRenderer (~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/util.js:153:10)
    at ~/code/clerk-astro-error/node_modules/astro/dist/runtime/server/render/astro/render-template.js:28:36
```
