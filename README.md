<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Quantile Function

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Degenerate distribution][degenerate-distribution] [quantile function][quantile-function].

<section class="intro">

The [quantile function][quantile-function] for a [degenerate][degenerate-distribution] random variable is

<!-- <equation class="equation" label="eq:degenerate_quantile_function" align="center" raw="Q(p;\mu) = \inf \left\{x \in {\mathbb {R}}:p \leq F(x;\mu)\right\} = \mu" alt="Quantile function for a degenerate distribution."> -->

```math
Q(p;\mu) = \inf \left\{x \in {\mathbb {R}}:p \leq F(x;\mu)\right\} = \mu
```

<!-- <div class="equation" align="center" data-raw-text="Q(p;\mu) = \inf \left\{x \in {\mathbb {R}}:p \leq F(x;\mu)\right\} = \mu" data-equation="eq:degenerate_quantile_function">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@e1fbdee688c5409e4cc6b0cd06d90b1cd2abd67c/lib/node_modules/@stdlib/stats/base/dists/degenerate/quantile/docs/img/equation_degenerate_quantile_function.svg" alt="Quantile function for a degenerate distribution.">
    <br>
</div> -->

<!-- </equation> -->

for `0 <= p <= 1` and where `µ` is the constant value of the distribution.

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import quantile from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-degenerate-quantile@v0.3.0-deno/mod.js';
```

You can also import the following named exports from the package:

```javascript
import { factory } from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-degenerate-quantile@v0.3.0-deno/mod.js';
```

#### quantile( p, mu )

Evaluates the [quantile function][quantile-function] of a [degenerate distribution][degenerate-distribution] centered at `mu`.

```javascript
var y = quantile( 0.3, 8.0 );
// returns 8.0

y = quantile( 0.9, 8.0 );
// returns 8.0
```

#### quantile.factory( mu )

Returns a function for evaluating the [quantile function][quantile-function] of a [degenerate distribution][degenerate-distribution] centered at `mu`.

```javascript
var myquantile = quantile.factory( 10.0 );

var y = myquantile( 0.2 );
// returns 10.0

y = myquantile( 1.1 );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import uniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-array-uniform@deno/mod.js';
import logEachMap from 'https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@deno/mod.js';
import quantile from 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-degenerate-quantile@v0.3.0-deno/mod.js';

var opts = {
    'dtype': 'float64'
};
var p = uniform( 10, 0.0, 1.0, opts );
var mu = uniform( 10, -5.0, 5.0, opts );

logEachMap( 'p: %0.4f, µ: %0.4f, Q(p;µ): %0.4f', p, mu, quantile );
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



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

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-degenerate-quantile.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-degenerate-quantile

[test-image]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/actions/workflows/test.yml/badge.svg?branch=v0.3.0
[test-url]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/actions/workflows/test.yml?query=branch:v0.3.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-degenerate-quantile/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-degenerate-quantile?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-degenerate-quantile.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-degenerate-quantile/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/tree/deno
[deno-readme]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/tree/umd
[umd-readme]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/tree/esm
[esm-readme]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/stats-base-dists-degenerate-quantile/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-degenerate-quantile/main/LICENSE

[quantile-function]: https://en.wikipedia.org/wiki/Quantile_function

[degenerate-distribution]: https://en.wikipedia.org/wiki/Degenerate_distribution

</section>

<!-- /.links -->
