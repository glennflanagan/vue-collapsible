[![Netlify Status](https://api.netlify.com/api/v1/badges/10d9afa3-016a-4707-9dcc-970a4e4a3ba9/deploy-status)](https://app.netlify.com/sites/vue-collapsible/deploys)
[![Npm Version](https://img.shields.io/npm/v/vue-collapsible-component.svg)](https://www.npmjs.com/package/vue-collapsible-component) [![License](https://img.shields.io/npm/l/vue-collapsible-component.svg)](https://github.com/glennflanagan/vue-collapsible/blob/master/LICENSE.md) [![Downloads Per Week](https://img.shields.io/npm/dw/vue-collapsible-component.svg)](https://npmcharts.com/compare/vue-collapsible-component)

# Vue Responsive Collapsible Section Component (Collapsible)

Vue component to wrap content in Collapsible element with trigger to open and close.

![Alt text](https://github.com/glennflanagan/vue-collapsible/raw/master/src/assets/collapsible.gif)

It's like an accordion, but where any number of sections can be open at the same time.

## [Demo](https://vue-collapsible.netlify.com/)

See the demo source code for code examples of how to use.

## Installation

Install via npm

```
npm install vue-collapsible-component
```

or yarn

```
yarn add vue-collapsible-component
```

Alternatively just download the `Collapsible.vue` file form the `src` folder and include it in your project in your chosen way.

## Usage

Collapsible can receive any HTML elements or Vue component as it's children. Collapsible will wrap the contents, as well as generate a trigger element which will control showing and hiding.

To customise the trigger element use the `trigger` slot for the open state, and `closedTrigger` slot for the closed state.

```html
<template>
  <Collapsible class="example-collapsible">
    <div slot="trigger">
      <div class="customTrigger">
        <h2>Custom open trigger element</h2>
      </div>
    </div>

    <div slot="closedTrigger">
      <div class="customTrigger">
        <h2>Custom closed trigger element</h2>
      </div>
    </div>

    <div id="example2">
      <p>
        Lorem ipsum dolor sit ...
      </p>
    </div>
  </Collapsible>
</template>

<script>
  import 'vue-collapsible-component/lib/vue-collapsible.css';
  import Collapsible from 'vue-collapsible-component';

  export default {
    components: {
      Collapsible,
    },
  };
</script>
```

## Props

These are the available overrides

---

#### `openLabel` `<String>`

Set the default trigger open label

---

#### `closedLabel` `<String>`

Set the default trigger close label

---

#### `transitionDuration` `<String>`

Override the default CSS transition duration. Example `500ms`

---

#### `transitionTimingFunction` `<String>`

Override the default CSS transition timing function. Example `ease-in-out`

---

#### `transitionDelay` `<String>`

Override the default CSS transition delay. Example `300ms`

---

#### `isOpen` `<Boolean>`

Sets the default open/closed state. Use this to control the open/close state programmatically.

---

#### `onCollapse` `<Function>`

Fired whenever the open/close state is changed with the new open/closed state.

---

## Licence

[MIT](LICENCE.md)

## Contributing

View the the [README](CONTRIBUTING.md)
