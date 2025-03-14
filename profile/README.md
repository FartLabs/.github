[![Discord invite](https://dcbadge.vercel.app/api/server/W39PG9t3nZ?style=flat)](https://go.fart.tools/chat)

# FartLabs - Software solutions out the wazoo 🧪

We develop software out the wazoo!

Our projects are designed to be fun, useful, and educational. We're always
looking for new contributors and collaborators, so feel free to reach out if
you're interested in joining the fun!

## Libraries

_Maintaining libraries on jsr.io_ -
[https://jsr.io/@fartlabs](https://jsr.io/@fartlabs)

- [**@fartlabs/jsonx**](https://github.com/FartLabs/jsonx): Cross-runtime JSX
  runtime and compiler library for composing JSON data.
- [**@fartlabs/ht**](https://github.com/FartLabs/ht): Type-safe HTML rendering
  library for Deno.
- [**@fartlabs/htx**](https://github.com/FartLabs/htx): Library of
  `@fartlabs/jsonx` components for composing HTML content.
- [**@fartlabs/rt**](https://github.com/FartLabs/rt): Minimal HTTP router
  library based on the
  [URLPattern API](https://developer.mozilla.org/en-US/docs/Web/API/URL_Pattern_API).
- [**@fartlabs/rtx**](https://github.com/FartLabs/rtx): Library of
  `@fartlabs/jsonx` components for composing `@fartlabs/rt` routers.

## More projects

- [**@fartlabs/deno_blocks**](https://github.com/FartLabs/deno_blocks):
  [Blockly](https://github.com/google/blockly) IDE integration with
  [Fresh](https://github.com/denoland/fresh) and Deno Subhosting. _Winner_ of
  [Deno Subhosting Hackathon](https://deno.com/blog/subhosting-hackathon) (Ryan
  Dahl's favorite).
- [**@fartlabs/jsonx_docs**](https://github.com/FartLabs/jsonx_docs):
  Documentation website and online code editor for the
  [`@fartlabs/jsonx`](https://github.com/FartLabs/jsonx) library.

## Quick examples

### [@fartlabs/jsonx](https://github.com/FartLabs/jsonx)

```tsx
function Cat() {
  return { animals: ["🐈"] };
}

function Dog() {
  return { animals: ["🐕"] };
}

const data = (
  <>
    <Cat />
    <Dog />
  </>
);

console.log(data); // { animals: ["🐈", "🐕"] }
```

Curious about jsonx? [Learn more...](https://jsonx.deno.dev)

### [@fartlabs/ht](https://github.com/FartLabs/ht)

```ts
import { a } from "@fartlabs/ht";

const html = a({ href: "https://jsr.io/@fartlabs/ht" }, "@fartlabs/ht");

Deno.writeTextFileSync("index.html", html);
```

### [@fartlabs/htx](https://github.com/FartLabs/htx)

```tsx
import { A, BODY, H1, P } from "@fartlabs/htx";

const html = (
  <BODY>
    <H1>Hello, World!</H1>
    <P>This is a paragraph.</P>
    <A href="https://jsr.io/@fartlabs/htx">@fartlabs/htx</A>
  </BODY>
);

Deno.writeTextFileSync("index.html", html);
```

### [@fartlabs/rt](https://github.com/FartLabs/rt)

```ts
import { Router } from "@fartlabs/rt";

const router = new Router()
  .get("/", () => new Response("Hello, World!"))
  .default(() => new Response("Not found", { status: 404 }));

Deno.serve((request) => router.fetch(request));
```

### [@fartlabs/rtx](https://github.com/FartLabs/rtx)

```tsx
import { Get, Router } from "@fartlabs/rtx";

const router = (
  <Router default={() => new Response("Not found", { status: 404 })}>
    <Get
      pattern="/"
      handle={() =>
        new Response("Hello, World!")}
    />
  </Router>
);

Deno.serve((request) => router.fetch(request));
```

## Get involved

We welcome contributions! Here's how:

- **Raise an issue:** Report bugs or suggest new features.
- **Submit a pull request:** Directly improve our code.
- **Join our community:** Discussions are open for questions and collaborations.

## Community

Reach out to us on Discord: <https://go.fart.tools/chat>.

## License

See the `LICENSE` file in each repository for details.

---

Maintained with ❤️ at **FartLabs** 🧪
