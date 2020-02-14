---
title: Markup
namespace: docs
layout: components/docs/docs
url: 'docs/userguide/markup/'
---


# @barba/core

Barba core manages your **page transitions** with ease.

## Markup

At the beginning, Barba needs to know a little bit about your **DOM structure**.
By default, it uses this markup structure in your pages:

```html
<body data-barba="wrapper">
  <!-- put here content that will not change
  between your pages, like <header> or <nav> -->

  <main data-barba="container" data-barba-namespace="home">
    <!-- put here the content you wish to change
    between your pages, like your main content <h1> or <p> -->
  </main>

  <!-- put here content that will not change
  between your pages, like <footer> -->
</body>
```

> Note that you can build the `html` in many ways, but keep in mind that the `wrapper` should always wrap the `container`

### Wrapper

The wrapper is **the main Barba section** that contains all your page structure and the Barba [container](#Container). Beware, everything inside of this wrapper and outside of the container **will not be updated by Barba**: you can put your `<header>`, `<footer>` or `<nav>` safely here. It is mainly defined on the `<body>` tag, but you can add it on a `div` or `section` for example.

### Container

The container defines **a section in which content is updated automatically** when you navigate between your pages. Beware, everything inside of this container **will be updated by Barba**: you can put your `<footer>` safely here. It is mainly defined on the `<main>` tag, but you can add it on a `div` or `section` for example.

### Namespace

The namespace allows you to define **a unique name for each page**. Barba mainly uses this namespace for transition [rules](/docs/userguide/syntax/#Rules) and [views](/docs/userguide/syntax/#lt-view-gt-object).

> Note: all **data-barba** attributes can be easily customized using the Barba [schema](/docs/userguide/syntax/#schema).