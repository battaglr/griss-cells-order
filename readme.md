# Griss cells order

Cells order module for [Griss](https://github.com/battaglr/griss/).

## Overview

Extends [Griss](https://github.com/battaglr/griss/) by adding a set of classes
that allows to change the default order of each cell, with three available
breakpoints to make adjustments at different screen widths.

Key features:

- Reorder cells using fluid size based on fractions.
- Responsive and mobile-first.
- Lightweight (~645 bytes minified and gzipped).
- Extensible using the different
  [available modules](https://github.com/battaglr/griss/#available-modules)
  or your own code.

## Installation

Install it using [npm](https://npmjs.com):

```sh
npm install griss-cells-order
```

Or simply [download the minified file](dist/griss-cells-order.min.css) and
include it into your project:

```html
<link href="griss-cells-order.min.css" rel="stylesheet" />
```

*You will also need to install
[Griss core module](https://github.com/battaglr/griss/#installation).*

## Usage

*Make sure you have read
[Griss core documentation](https://github.com/battaglr/griss/#usage) first.*

Combine the base cell class —`gs-Grid-cell`— with the the push or pull classes.

The push class —i.e. `gs-Grid-cell--push(1/2)`— will move cells to the right
while the pull class —i.e. `gs-Grid-cell--pull(2/3)`— will move cells to
the left.

To define the size of each pull or push you can choose any fraction from halves
to sixths. If you need to return to the original order you can use the value
*none* represented as `n` —i.e. `gs-Grid-cell--push(n)`.

If you need to make adjustments at different screen widths use any of the
available breakpoint suffixes: `@s`, `@m` and `@l` —i.e.
`gs-Grid-cell--pull(1/2)@m`.

#### Examples

Some basic examples:

- Move cell one third to the right:

  ```html
  <div class="gs-Grid">
    <div class="gs-Grid-cell gs-Grid-cell--size(1/3)"> ... </div>
    <div class="gs-Grid-cell gs-Grid-cell--size(1/3) gs-Grid-cell--push(1/3)"> ... </div>
  </div>
  ```

- Reverse cells order:

  ```html
  <ul class="gs-Grid">
    <li class="gs-Grid-cell gs-Grid-cell--size(1/2) gs-Grid-cell--push(1/2)"> ... </li>
    <li class="gs-Grid-cell gs-Grid-cell--size(1/2) gs-Grid-cell--pull(1/2)"> ... </li>
  </ul>
  ```

- Reverse cells order at medium breakpoint:

  ```html
  <div class="gs-Grid">
    <div class="gs-Grid-cell gs-Grid-cell--size(1/2) Grid-cell--push(1/2)@m"> ... </div>
    <div class="gs-Grid-cell gs-Grid-cell--size(1/2) Grid-cell--pull(1/2)@m"> ... </div>
  </div>
  ```

For more examples, please check out the
[test page](https://battaglr.github.io/griss-cells-order/test/test.html).

#### Available classes

##### Base

- `gs-Grid-cell--push(1/2)`
- `gs-Grid-cell--pull(1/2)`
- `gs-Grid-cell--push(1/3)`
- `gs-Grid-cell--pull(1/3)`
- `gs-Grid-cell--push(2/3)`
- `gs-Grid-cell--pull(2/3)`
- `gs-Grid-cell--push(1/4)`
- `gs-Grid-cell--pull(1/4)`
- `gs-Grid-cell--push(2/4)`
- `gs-Grid-cell--pull(2/4)`
- `gs-Grid-cell--push(3/4)`
- `gs-Grid-cell--pull(3/4)`
- `gs-Grid-cell--push(1/5)`
- `gs-Grid-cell--pull(1/5)`
- `gs-Grid-cell--push(2/5)`
- `gs-Grid-cell--pull(2/5)`
- `gs-Grid-cell--push(3/5)`
- `gs-Grid-cell--pull(3/5)`
- `gs-Grid-cell--push(4/5)`
- `gs-Grid-cell--pull(4/5)`
- `gs-Grid-cell--push(1/6)`
- `gs-Grid-cell--pull(1/6)`
- `gs-Grid-cell--push(2/6)`
- `gs-Grid-cell--pull(2/6)`
- `gs-Grid-cell--push(3/6)`
- `gs-Grid-cell--pull(3/6)`
- `gs-Grid-cell--push(4/6)`
- `gs-Grid-cell--pull(4/6)`
- `gs-Grid-cell--push(5/6)`
- `gs-Grid-cell--pull(5/6)`

##### Breakpoints

- `gs-Grid-cell--push(n)@s`
- `gs-Grid-cell--pull(n)@s`
- `gs-Grid-cell--push(n/n)@s`
- `gs-Grid-cell--pull(n/n)@s`
- `gs-Grid-cell--push(n)@m`
- `gs-Grid-cell--pull(n)@m`
- `gs-Grid-cell--push(n/n)@m`
- `gs-Grid-cell--pull(n/n)@m`
- `gs-Grid-cell--push(n)@l`
- `gs-Grid-cell--pull(n)@l`
- `gs-Grid-cell--push(n/n)@l`
- `gs-Grid-cell--pull(n/n)@l`

*`n` stands for “none” and `n/n` should be replaced with an available fraction.*

## Browser support

The following browsers are supported:

- Chrome *latest 5*
- Firefox *latest 5*
- Internet Explorer *8+*
- Edge *latest 5*
- Opera *latest 5*
- Safari *latest 5*
- iOS Safari *latest 5*
- Android Browser *2.1+*

*IE8 does not support media queries.*

## Contributing

Contributions are welcome! Please, read the
[contribution guidelines](contributing.md) first.

## License

Released under the [MIT license](license.txt).
