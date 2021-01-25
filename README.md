# myHP Style Guide
## Technologies Table of Contents

  1. [JavaScript](#javacript)
  1. [TypeScript](#typescript)
  1. [React](#react)
  1. [Hooks](#hooks)
  1. [Redux](#redux)
  1. [ReduxSaga](#redux-saga)
  1. [Immer](#immer)
  1. [Storybook](#storybook)
   
# JavaScript
## JavaScript Table of Contents

  1. [References](#references)
  1. [Strings](#strings)
  2. [Links](#links)
## References

  <a name="references--prefer-const"></a><a name="2.1"></a>
  - [2.1](#references--prefer-const) Use `const` for all of your references; avoid using `var`. eslint: [`prefer-const`](https://eslint.org/docs/rules/prefer-const.html), [`no-const-assign`](https://eslint.org/docs/rules/no-const-assign.html)

    > Why? This ensures that you can’t reassign your references, which can lead to bugs and difficult to comprehend code.

    ```javascript
    // bad
    var a = 1;
    var b = 2;

    // good
    const a = 1;
    const b = 2;
    ```

  <a name="references--disallow-var"></a><a name="2.2"></a>
  - [2.2](#references--disallow-var) If you must reassign references, use `let` instead of `var`. eslint: [`no-var`](https://eslint.org/docs/rules/no-var.html)

    > Why? `let` is block-scoped rather than function-scoped like `var`.

    ```javascript
    // bad
    var count = 1;
    if (true) {
      count += 1;
    }

    // good, use the let.
    let count = 1;
    if (true) {
      count += 1;
    }
    ```

  <a name="references--block-scope"></a><a name="2.3"></a>
  - [2.3](#references--block-scope) Note that both `let` and `const` are block-scoped.

    ```javascript
    // const and let only exist in the blocks they are defined in.
    {
      let a = 1;
      const b = 1;
    }
    console.log(a); // ReferenceError
    console.log(b); // ReferenceError
    ```

**[⬆ back to top](#javascript-table-of-contents)**
## Strings

  <a name="strings--quotes"></a><a name="6.1"></a>
  - [6.1](#strings--quotes) Use single quotes `''` for strings. eslint: [`quotes`](https://eslint.org/docs/rules/quotes.html)

    ```javascript
    // bad
    const name = "Capt. Janeway";

    // bad - template literals should contain interpolation or newlines
    const name = `Capt. Janeway`;

    // good
    const name = 'Capt. Janeway';
    ```

  <a name="strings--line-length"></a><a name="6.2"></a>
  - [6.2](#strings--line-length) Strings that cause the line to go over 100 characters should not be written across multiple lines using string concatenation.

    > Why? Broken strings are painful to work with and make code less searchable.

    ```javascript
    // bad
    const errorMessage = 'This is a super long error that was thrown because \
    of Batman. When you stop to think about how Batman had anything to do \
    with this, you would get nowhere \
    fast.';

    // bad
    const errorMessage = 'This is a super long error that was thrown because ' +
      'of Batman. When you stop to think about how Batman had anything to do ' +
      'with this, you would get nowhere fast.';

    // good
    const errorMessage = 'This is a super long error that was thrown because of Batman. When you stop to think about how Batman had anything to do with this, you would get nowhere fast.';
    ```

  <a name="es6-template-literals"></a><a name="6.4"></a>
  - [6.3](#es6-template-literals) When programmatically building up strings, use template strings instead of concatenation. eslint: [`prefer-template`](https://eslint.org/docs/rules/prefer-template.html) [`template-curly-spacing`](https://eslint.org/docs/rules/template-curly-spacing)

    > Why? Template strings give you a readable, concise syntax with proper newlines and string interpolation features.

    ```javascript
    // bad
    function sayHi(name) {
      return 'How are you, ' + name + '?';
    }

    // bad
    function sayHi(name) {
      return ['How are you, ', name, '?'].join();
    }

    // bad
    function sayHi(name) {
      return `How are you, ${ name }?`;
    }

    // good
    function sayHi(name) {
      return `How are you, ${name}?`;
    }
    ```

  <a name="strings--eval"></a><a name="6.5"></a>
  - [6.4](#strings--eval) Never use `eval()` on a string, it opens too many vulnerabilities. eslint: [`no-eval`](https://eslint.org/docs/rules/no-eval)

  <a name="strings--escaping"></a>
  - [6.5](#strings--escaping) Do not unnecessarily escape characters in strings. eslint: [`no-useless-escape`](https://eslint.org/docs/rules/no-useless-escape)

    > Why? Backslashes harm readability, thus they should only be present when necessary.

    ```javascript
    // bad
    const foo = '\'this\' \i\s \"quoted\"';

    // good
    const foo = '\'this\' is "quoted"';
    const foo = `my name is '${name}'`;
    ```
    **[⬆ back to section top](#javascript-table-of-contents)**  
## Links
[Airbnb Style Guide](https://github.com/airbnb/javascript)  
**[⬆ back to top](#technologies-table-of-contents)** 
  
# TypeScript
## Examples
## Links
[The Typescript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)  
**[⬆ back to top](#technologies-table-of-contents)** 
  
# React
## Examples
## Links
[Airbnb Style Guide](https://github.com/airbnb/javascript/tree/master/react)  
[Patterns](https://reactpatterns.com/)  
[Component Patterns Links](https://github.com/markerikson/react-redux-links/blob/master/react-component-patterns.md)  
## People
[Dan Abramov (React)](https://overreacted.io/)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Hooks
## Examples
## Links
[Introduction](https://reactjs.org/docs/hooks-intro.html)  
[A Complete Guide to useEffect](https://overreacted.io/a-complete-guide-to-useeffect/)  
## Videos
[React Today and Tomorrow and 90% Cleaner React with Hooks](https://youtu.be/dpw9EHDh2bM)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Redux
## Links
[Overview](https://redux.js.org/tutorials/essentials/part-1-overview-concepts)  
[Fundamentals](https://redux.js.org/tutorials/fundamentals/part-1-overview)  
[Style Guide](https://redux.js.org/style-guide/style-guide)  
## People
[Mark Erikson (Redux)](https://blog.isquaredsoftware.com/)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Redux Saga
## Links
[Introduction](https://redux-saga.js.org/docs/introduction/)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Immer
## Links
[Introduction](https://immerjs.github.io/immer/docs/introduction)  
[Update Patterns](https://immerjs.github.io/immer/docs/update-patterns)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Storybook
## Links
[Introduction](https://storybook.js.org/docs/react/get-started/introduction)  
**[⬆ back to top](#technologies-table-of-contents)** 



