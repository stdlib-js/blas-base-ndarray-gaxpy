<!--

@license Apache-2.0

Copyright (c) 2026 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# gaxpy

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Multiply a one-dimensional ndarray `x` by a constant `alpha` and add the result to a one-dimensional ndarray `y`.

<section class="intro">

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import gaxpy from 'https://cdn.jsdelivr.net/gh/stdlib-js/blas-base-ndarray-gaxpy@esm/index.mjs';
```

#### gaxpy( arrays )

Multiplies a one-dimensional ndarray `x` by a constant `alpha` and adds the result to a one-dimensional ndarray `y`.

```javascript
import vector from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-vector-ctor@esm/index.mjs';
import scalar2ndarray from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-from-scalar@esm/index.mjs';

var x = vector( [ 1.0, 2.0, 3.0, 4.0, 5.0 ], 'generic' );
var y = vector( [ 1.0, 1.0, 1.0, 1.0, 1.0 ], 'generic' );

var alpha = scalar2ndarray( 5.0, {
    'dtype': 'generic'
});

var z = gaxpy( [ x, y, alpha ] );
// returns <ndarray>[ 6.0, 11.0, 16.0, 21.0, 26.0 ]

var bool = ( z === y );
// returns true
```

The function has the following parameters:

-   **arrays**: array-like object containing the following ndarrays:

    -   a one-dimensional input ndarray.
    -   a one-dimensional output ndarray.
    -   a zero-dimensional ndarray containing a scalar constant.

</section>

<!-- /.usage -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import discreteUniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-discrete-uniform@esm/index.mjs';
import scalar2ndarray from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-from-scalar@esm/index.mjs';
import ndarray2array from 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-to-array@esm/index.mjs';
import gaxpy from 'https://cdn.jsdelivr.net/gh/stdlib-js/blas-base-ndarray-gaxpy@esm/index.mjs';

var opts = {
    'dtype': 'generic'
};

var x = discreteUniform( [ 10 ], 0, 100, opts );
console.log( ndarray2array( x ) );

var y = discreteUniform( [ 10 ], 0, 10, opts );
console.log( ndarray2array( y ) );

var alpha = scalar2ndarray( 5.0, opts );

var out = gaxpy( [ x, y, alpha ] );
console.log( ndarray2array( out ) );

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/blas-base-ndarray-gaxpy.svg
[npm-url]: https://npmjs.org/package/@stdlib/blas-base-ndarray-gaxpy

[test-image]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/blas-base-ndarray-gaxpy/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/blas-base-ndarray-gaxpy?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/blas-base-ndarray-gaxpy.svg
[dependencies-url]: https://david-dm.org/stdlib-js/blas-base-ndarray-gaxpy/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/tree/deno
[deno-readme]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/tree/umd
[umd-readme]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/tree/esm
[esm-readme]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/blas-base-ndarray-gaxpy/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/blas-base-ndarray-gaxpy/main/LICENSE

</section>

<!-- /.links -->
