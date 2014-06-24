Bootsoft guide to CSS / LESS / SCSS {

*A Code Style Guide to CSS*


## Table of Contents

  1. [Spacing](#spacing)
  1. [Formatting](#formatting)
  1. [Nesting](#nesting)
  1. [Font Sizing](#font-sizing)
  1. [License](#license)

## Spacing

  - Use soft-tabs with a two space indent. Spaces are the only way to guarantee code renders the same in any person's environment.
  - Put spaces after `:` in property declarations.
  - Put spaces before `{` in rule declarations.
  - Put line breaks between rulesets.
  - When grouping selectors, keep individual selectors to a single line.
  - Place closing braces of declaration blocks on a new line.
  - Each declaration should appear on its own line for more accurate error reporting.


**[⬆ back to top](#table-of-contents)**


## Formating

  - Colors
    - HEX is most widely supported format in terms of browers, and is easily copied / pasted, however it does not support the alpha channel, therefor when alpha channel is not needed, use hex.
    - Use HSLa over RGBa for purposes of ease of use, both are supported equally in browsers.
  - Use `//` for comments in LESS / SCSS instead of /**/
  - Avoid specifying units for zero values, e.g., `margin: 0;` instead of `margin: 0px;`.
  - Strive to limit use of shorthand declarations to instances where you must explicitly set all the available values.


**[⬆ back to top](#table-of-contents)**


## Nesting

  In vanilla CSS the practice of adding speceficity to a rule can be handled be including parent class names.  In CSS pre-processors a developer may nest style declarations such that the compiled CSS will prepend the parent class to the rule, thereby elimnating the repetition of parent class names.

  ```css
  /*Vanilla CSS*/
  .my-class {
    color : '#000';
  }

  .my-other-class {
    color : '#eaeaea';
  }

  .parent-context-class .my-class,
  .parent-context-class .my-other-class {
    color : '#fff';
  }

  ```

  ```scss
  //SCSS
  .my-class {
    color : '#000'
  }

  .my-other-class {
    color : '#eaeaea';
  }

  .parent-context-class {

  	.my-class,
  	.my-other-class {
      color : '#fff'
  	}

  }
  ```
  This is a very powerful feature of the precompiled languages.  It should not be abused as over-nesting can result in bloated code.


**[⬆ back to top](#table-of-contents)**


## Font Sizing

  - The base font size of the body should be 62.5% to more easily allow all relative font measurements to be relative to that.
  - Developers should use the rem (or root em) unit to define font sizes.
  - CSS declaration where IE8 support is must have a pixel fallback.

  ```css
  //body style declaration
  
  body {
  	font-family : 'Arial, Sans-Serif',
  	font-size : 62.5%
  }

  //20px for IE8 and all Moder browsers
  h1 {
    font-size : 20px;
    font-size : 2rem;
  }
  ```


## License

(The MIT License)

Copyright (c) 2014 Bootsoft

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

**[⬆ back to top](#table-of-contents)**

# }
