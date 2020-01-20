<p align="center">
  <img src="/assets/swal2-logo.png" alt="SweetAlert2">
</p>

<p align="center">
  FIXED JSDOC ISSUE!
</p>

<p align="center">
  A beautiful, responsive, customizable, accessible (WAI-ARIA) replacement for JavaScript's popup boxes. Zero dependencies.
</p>

<p align="center">
  <a href="https://sweetalert2.github.io/">
    <img src="https://raw.github.com/sweetalert2/sweetalert2/master/assets/sweetalert2.gif" width="562"><br>
    See SweetAlert2 in action ↗
  </a>
</p>

<p align="center">
  <a href="https://github.com/sweetalert2/sweetalert2/actions"><img alt="Build Status" src="https://github.com/sweetalert2/sweetalert2/workflows/build/badge.svg"></a>
  <a href="https://codeclimate.com/github/sweetalert2/sweetalert2/test_coverage"><img alt="Coverage Status" src="https://api.codeclimate.com/v1/badges/eba34bb80477933854d4/test_coverage"></a>
  <a href="https://www.npmjs.com/package/sweetalert2"><img alt="Version" src="https://img.shields.io/npm/v/sweetalert2.svg"></a>
  <a href="https://www.jsdelivr.com/package/npm/sweetalert2"><img alt="jsdelivr" src="https://data.jsdelivr.com/v1/package/npm/sweetalert2/badge?style=rounded"></a>
  <a href="#support-and-donations"><img alt="Support Donate" src="https://ionicabizau.github.io/badges/paypal.svg"></a>
</p>

---

:shipit: The author of SweetAlert2 ([@limonte](https://github.com/limonte/)) is looking for short-term to medium-term working contracts in front-end, preferably OSS.

---

:point_right: **Upgrading from v8.x to v9.x?** [Read the release notes!](https://github.com/sweetalert2/sweetalert2/releases/tag/v9.0.0)
<br>If you're upgrading from v7.x, please [upgrade from v7 to v8](https://github.com/sweetalert2/sweetalert2/releases/tag/v8.0.0) first!
<br>If you're upgrading from v6.x, please [upgrade from v6 to v7](https://github.com/sweetalert2/sweetalert2/releases/tag/v7.0.0) first!

:point_right: **Migrating from [SweetAlert](https://github.com/t4t5/sweetalert)?** [SweetAlert 1.x to SweetAlert2 migration guide](https://github.com/sweetalert2/sweetalert2/wiki/Migration-from-SweetAlert-to-SweetAlert2)

---

Installation
------------

```sh
npm install --save ngx-angular8-sweetalert2
```

Or grab from [jsdelivr CDN](https://www.jsdelivr.com/package/npm/sweetalert2)
:

```html
<script src="https://cdn.jsdelivr.net/npm/sweetalert2@9"></script>
```


Usage
-----

```html
<script src="ngx-angular8-sweetalert2/dist/sweetalert2.all.min.js"></script>

<!-- Include a polyfill for ES6 Promises (optional) for IE11 -->
<script src="https://cdn.jsdelivr.net/npm/promise-polyfill9/dist/polyfill.js"></script>
```

You can also include the stylesheet separately if desired:

```html
<script src="sweetalert2/dist/sweetalert2.min.js"></script>
<link rel="stylesheet" href="sweetalert2/dist/sweetalert2.min.css">
```

Or:

```js
// ES6 Modules or TypeScript
import Swal from 'ngx-angular8-sweetalert2'

// CommonJS
const Swal = require('ngx-angular8-sweetalert2')
```

Or with JS modules:

```html
<link rel="stylesheet" href="ngx-angular8-sweetalert2/dist/sweetalert2.css">

<script type="module">
  import Swal from 'ngx-angular8-sweetalert2/src/sweetalert2.js'
</script>
```

It's possible to import JS and CSS separately, e.g. if you need to customize styles:

```js
import Swal from 'ngx-angular8-sweetalert2/dist/sweetalert2.js'

import 'ngx-angular8-sweetalert2/src/sweetalert2.scss'
```

Please note that [TypeScript is well-supported](https://github.com/sweetalert2/sweetalert2/blob/master/sweetalert2.d.ts), so you don't have to install a third-party declaration file.


Examples
--------

The most basic message:

```js
Swal.fire('Hello world!')
```

A message signaling an error:

```js
Swal.fire('Oops...', 'Something went wrong!', 'error')
```

Handling the result of SweetAlert2 modal:

```js
Swal.fire({
  title: 'Are you sure?',
  text: 'You will not be able to recover this imaginary file!',
  icon: 'warning',
  showCancelButton: true,
  confirmButtonText: 'Yes, delete it!',
  cancelButtonText: 'No, keep it'
}).then((result) => {
  if (result.value) {
    Swal.fire(
      'Deleted!',
      'Your imaginary file has been deleted.',
      'success'
    )
  // For more information about handling dismissals please visit
  // https://sweetalert2.github.io/#handling-dismissals
  } else if (result.dismiss === Swal.DismissReason.cancel) {
    Swal.fire(
      'Cancelled',
      'Your imaginary file is safe :)',
      'error'
    )
  }
})
```

## [Go here to see the docs and more examples ↗](https://sweetalert2.github.io/)


Browser compatibility
---------------------

 IE11* | Edge | Chrome | Firefox | Safari | Opera | UC Browser
-------|------|--------|---------|--------|-------|------------
:heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |

\* ES6 Promise polyfill should be included, see [usage example](#usage).

Note that SweetAlert2 **does not** and **will not** provide support or functionality of any kind on IE10 and lower.



## For company Indeema Software
