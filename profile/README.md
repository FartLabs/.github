# @FartLabs - Software solutions out the wazoo 🧪

We develop software out the wazoo! Our projects are designed to be fun, useful,
and educational. We're always looking for new contributors and collaborators, so
feel free to reach out if you're interested in joining the fun!

## Libraries on jsr.io

_Maintaining libraries on jsr.io_ -
[https://jsr.io/@fartlabs](https://jsr.io/@fartlabs)

- [**@fartlabs/jsonx**](https://github.com/FartLabs/jsonx): Cross-runtime JSX
  runtime and compiler library for composing JSON data.
- [**@fartlabs/rtx**](https://github.com/FartLabs/rtx): Minimal HTTP router
  library based on the
  [URLPattern API](https://developer.mozilla.org/en-US/docs/Web/API/URL_Pattern_API).

## More projects

- [**@FartLabs/deno_blocks**](https://github.com/FartLabs/deno_blocks):
  [Blockly](https://github.com/google/blockly) IDE integration with
  [Fresh](https://github.com/denoland/fresh) and Deno Subhosting. Winner of
  [Deno Subhosting Hackathon](https://deno.com/blog/subhosting-hackathon).
- [**@FartLabs/jsonx_docs**](https://github.com/FartLabs/jsonx_docs):
  _Documentation website_ and _playgrounds_ for the `@fartlabs/jsonx` library.

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

Deno.writeTextFileSync(
  "data.json",
  JSON.stringify(data, null, 2),
);
```

## Get involved

We welcome contributions! Here's how:

- **Raise an issue:** Report bugs or suggest new features.
- **Submit a pull request:** Directly improve our code.
- **Join our community:** Discussions are open for questions and collaborations.

## License

(See each repository's LICENSE file for details)

---

Maintained with ❤️ **@FartLabs**
