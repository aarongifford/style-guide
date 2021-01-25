# In Process Best Practices / Style Guide
## Technologies Table of Contents

  1. [JavaScript](#javacript)
  1. [TypeScript](#typescript)
  1. [React](#react)
  1. [Hooks](#hooks)
  1. [Redux](#redux)
  1. [ReduxSaga](#redux-saga)
  1. [Jest](#jest)
  1. [Storybook](#storybook)
   
# JavaScript
## JavaScript Table of Contents

  1. [References](#references)
  1. [Strings](#strings)
  1. [JavaScript Links](#javascript-links)
## References

  <a name="references--prefer-const"></a><a name="1.1"></a>
  - [1.1](#references--prefer-const) Use `const` for all of your references; avoid using `var`.

    > Why? This ensures that you can’t reassign your references, which can lead to bugs and difficult to comprehend code.

    ```javascript
    // bad
    var a = 1;
    var b = 2;

    // good
    const a = 1;
    const b = 2;
    ```

  <a name="references--disallow-var"></a><a name="1.2"></a>
  - [1.2](#references--disallow-var) If you must reassign references, use `let` instead of `var`.

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

  <a name="references--block-scope"></a><a name="1.3"></a>
  - [1.3](#references--block-scope) Note that both `let` and `const` are block-scoped.

    ```javascript
    // const and let only exist in the blocks they are defined in.
    {
      let a = 1;
      const b = 1;
    }
    console.log(a); // ReferenceError
    console.log(b); // ReferenceError
    ```

  **[⬆ back to section top](#javascript-table-of-contents)**
## Strings

  <a name="strings--quotes"></a><a name="2.1"></a>
  - [2.1](#strings--quotes) Use single quotes `''` for strings.

    ```javascript
    // bad
    const name = "Capt. Janeway";

    // bad - template literals should contain interpolation or newlines
    const name = `Capt. Janeway`;

    // good
    const name = 'Capt. Janeway';
    ```
  <a name="es6-template-literals"></a><a name="2.2"></a>
  - [2.2](#es6-template-literals) When programmatically building up strings, use template strings instead of concatenation.

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
  **[⬆ back to section top](#javascript-table-of-contents)**  
## JavaScript Links
[Airbnb Style Guide](https://github.com/airbnb/javascript)  
**[⬆ back to top](#technologies-table-of-contents)** 

# TypeScript
## Examples
## Links
[The Typescript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)  
**[⬆ back to top](#technologies-table-of-contents)** 
  
# React
## React Table of Contents

  1. [Props](#props)
  1. [Testing](#react-testing)
  1. [React Links](#react-links)

## Props
  <a name="react-props-case"></a><a name="1.1"></a>
  - [1.1](#react-props-case) Always use camelCase for prop names, or PascalCase if the prop value is a React component.
    ```javascript
    // bad
    <Foo
      UserName="hello"
      phone_number={12345678}
    />

    // good
    <Foo
      userName="hello"
      phoneNumber={12345678}
      Component={SomeComponent}
    />
    ```

    - [1.1] Always use camelCase for prop names, or PascalCase if the prop value is a React component.

    ```javascript
    // bad
    <Foo
      UserName="hello"
      phone_number={12345678}
    />

    // good
    <Foo
      userName="hello"
      phoneNumber={12345678}
      Component={SomeComponent}
    />
    ```
  **[⬆ back to section top](#javascript-table-of-contents)**  
## React Links
[Airbnb Style Guide](https://github.com/airbnb/javascript/tree/master/react)  
[React Patterns](https://reactpatterns.com/)  
[Component Patterns Links](https://github.com/markerikson/react-redux-links/blob/master/react-component-patterns.md)  
## People
[Dan Abramov (React)](https://overreacted.io/)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Hooks
## Examples
## Hooks Links
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

# Jest
## Links
[Testing React Apps](https://jestjs.io/docs/en/tutorial-react)  
[Testing React Native Apps](https://jestjs.io/docs/en/tutorial-react-native)  
**[⬆ back to top](#technologies-table-of-contents)** 
   
# Storybook
## Links
[Introduction](https://storybook.js.org/docs/react/get-started/introduction)  
**[⬆ back to top](#technologies-table-of-contents)** 



