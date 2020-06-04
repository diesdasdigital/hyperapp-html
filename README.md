# @diesdasdigital/hyperapp-html

[![npm](https://img.shields.io/npm/v/@diesdasdigital/hyperapp-html.svg)](https://www.npmjs.org/package/@diesdasdigital/hyperapp-html)

**NOTE:** This is a fork of [Swizz/hyperapp-html](https://github.com/Swizz/hyperapp-html) to provide better types for Typescript:
- allow lazy components
- allow passing a single `VNode` as children

Html helper functions for [Hyperapp](https://github.com/hyperapp/hyperapp). Use @diesdasdigital/hyperapp-html as an alternative to JSX or the <samp>hyperapp.h</samp> function.

## Installation

<pre>
yarn add <a href=https://www.npmjs.com/package/@diesdasdigital/hyperapp-html>@diesdasdigital/hyperapp-html</a>
</pre>

## Usage

Here is a counter that can be incremented or decremented. Go ahead and [try it online](https://codepen.io/jorgebucaran/pen/MrBgMy?editors=0010).

```jsx
import { h, app } from "hyperapp"
import { div, h1, button } from "@diesdasdigital/hyperapp-html"

const state = {
  count: 0
}

const actions = {
  down: () => state => ({ count: state.count - 1 }),
  up: () => state => ({ count: state.count + 1 })
}

const view = (state, actions) =>
  div([
    h1(state.count),
    button({ onclick: actions.down }, "-"),
    button({ onclick: actions.up }, "+")
  ])

app(state, actions, view, document.body)
```

See [/vars.json](/vars.json) for the list of available Html tags you can use in your program.


## License

@diesdasdigital/hyperapp-html is MIT licensed. See [LICENSE](LICENSE.md).
