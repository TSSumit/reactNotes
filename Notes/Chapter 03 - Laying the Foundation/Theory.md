# Chapter 03 - Laying the Foundation

## Q: browserlist

- Browserlist in React is a vital setup for optimizing how our code works on different web browsers.
- Tools like Babel and Autoprefixer use this setup to make sure our code works smoothly across various browsers.
- Its main job is to translate newer JavaScript code and add necessary styling tweaks, ensuring compatibility with a wide range of browsers.
- This setup is crucial for specifying which browser versions we're targeting and adapting to changes, making our development process strong and flexible.
- In a nutshell, browserlist is a must-have for making sure our code works well on different browsers, letting us use the latest coding techniques effectively.

## Q: Pollyfill

* To make older browsers undestand our new code, the new code is converted into a older code which browser can understand called pollyfill.
* `babel` do thid conversion automatically
* eg: ES6 is the newer version of javascript. If I'm working on 1999 browser, my browser will not understand what is this const, newPromise etc
* so, there is a replacement code for these functionalities which is compatible with older version of browers
* "browserslit" determine which browser can understand this code

## Q: Babel ?

"Babel is a JavaScript package or library used to transform code written in a newer version of JavaScript (ECMAScript) into code that can be executed in older JavaScript versions."

## Q: What is `JSX`?

* JSX stands for JavaScript XML.
* JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement() and/or appendChild() methods.
* JSX makes it easier to write and add HTML in React.
* JSX converts HTML tags into react elements.

#### Example 1 using JSX:

```
const myElement = <h1>I Love JSX!</h1>;
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

### Example 2 Without JSX:

```
const myElement = React.createElement('h1', {}, 'I do not use JSX!');
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

## Q: Superpowers of `JSX`.

A: Using JSX, you can write `markup inside Javascript`, providing you with a superpower to write logic and markup of a component inside a single .jsx file. JSX is easy to maintain and debug.

### Example

```
function greeting(user) {
//JSX
  return <h1>{user}, How are you!!!</h1>;
}
```

## Q: Role of `type` attribute in script tag? What options can I use there?

A: The `type` attribute specifies the type of the script. The type attribute identifies the content between the `<script>` and `</script>` tags. It has a Default value which is “text/javascript”.

### `type` attribute can be of the following types:

- `text/javascript` : It is the basic standard of writing javascript code inside the `<script>` tag.### Syntax

  ```
  <script type="text/javascript"></script>
  ```
- `text/ecmascript` : this value indicates that the script is following the `EcmaScript` standards.
- `module`: This value tells the browser that the script is a module that can import or export other files or modules inside it.
- `text/babel` : This value indicates that the script is a babel type and required bable to transpile it.
- `text/typescript`: As the name suggest the script is written in `TypeScript`.

## Q: `{TitleComponent}` vs `{<TitleComponent/>}` vs `{<TitleComponent></TitleComponent>}` in `JSX`.

A: The Difference is stated below:

- `{TitleComponent}`: This value describes the `TitleComponent` as a javascript expression or a variable.
  The `{}` can embed a javascript expression or a variable inside it.
- `<TitleComponent/>` : This value represents a Component that is basically returning Some JSX value. In simple terms `TitleComponent` a function that is returning a JSX value.
  A component is written inside the `{<  />}` expression.
- `<TitleComponent></TitleComponent>` :  `<TitleComponent />` and `<TitleComponent></TitleComponent>` are equivalent only when `< TitleComponent />` has no child components. The opening and closing tags are created to include the child components.

### Example

```
<TitleComponent>
    <FirstChildComponent />
    <SecondChildComponent />
    <ThirdChildComponent />
</TitleComponent>
```