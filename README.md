# JavaScript Hacking: A comprehensible guide

JavaScript is a powerful and versatile programming language that is widely used on the web for various purposes, such as validating form input, creating interactive content, and tracking user behavior. However, JavaScript can also be used by attackers to compromise the security of a website or web application.

I assume you have a basic understanding of JavaScript, including things like variables, data types, type conversion, basic operators, comparisons, conditional branching: `if` and `?`, logical operators, loops, switch statements, functions and parameters, and arrow functions

## What we'll cover:

- DOM
- API's
- Sessions & Cookies
- Security Protocols
- Encryption
- Strategies

### The Document Object Model (DOM)

The Document Object Model (DOM) is a tree-like structure that represents the content and layout of a webpage. It allows developers to manipulate the content and styling of a webpage using JavaScript.

#### DOM Nodes
The DOM is made up of a hierarchy of nodes, which can represent elements, attributes, and text content on a webpage. Here is a simplified representation of the structure of a DOM:

```
Document
  |- Element
  |  |- Attribute
  |  |- Element
  |  |  |- Text node
  |  |- Element
  |     |- Attribute
  |     |- Text node
  |- Element
  |  |- Text node
  |- Element
     |- Attribute
     |- Text node
```
Here are some common DOM nodes and their characteristics:

| Node | Description |
| ----------- | ----------- |
| Document | The root node of the DOM, representing the entire document. |
| Element | A node that represents an HTML element, such as a `div`, `p`, or `a`. |
| Attribute | A node that represents an attribute of an HTML element, such as the `src` attribute of an `img` element.  Typically displayed as `<element attribute="value">` |
| Text | A node that represents the text content of an element. Defined as `<element>text content</element>` |

Each node in the DOM has properties and methods that can be accessed and manipulated using JavaScript. Here are some common properties and methods for DOM nodes:

| Node | Properties | Methods|
| ----------- | ----------- | ----------- |
| Document | - | `getElementById()`<br>`getElementsByClassName()`<br>`getElementsByTagName()`<br>`querySelector()`<br>`querySelectorAll()` |
| Element | `innerHTML`<br>`textContent`<br>`className`<br>`style` | `appendChild()`<br>`removeChild()`<br>`replaceChild()`<br>`insertBefore()` |
| Attribute | `name`<br>`value` | - |
| Text | `nodeValue` | - |

#### DOM Method Usage

How to use the previously mentioned methods for accessing DOM Nodes

- `document.getElementById()`: This method allows you to access a node by its unique ID attribute. It returns the first element that has the specified ID, or null if no such element exists.
```javascript
const element = document.getElementById("myId");
```
- `document.getElementsByClassName()`: This method returns a collection of nodes with a given class name.
```javascript
const elements = document.getElementsByClassName("myClass");
```
- `document.getElementsByTagName()`: This method returns a collection of nodes with a given tag name.
```javascript
const elements = document.getElementsByTagName("p");
```
- `document.querySelector()`: This method returns the first node that matches a CSS selector.
```javascript
const element = document.querySelector("#myId .myClass");
```
- `document.querySelectorAll()`: This method returns a collection of nodes that match a CSS selector.
```javascript
const elements = document.querySelectorAll("p.myClass");
```

#### Website Manipulation

The DOM allows you to modify the content and layout of a webpage using JavaScript. Here are some common techniques for manipulating the DOM:

- Adding, deleting, or modifying elements: You can use the `createElement()`, `appendChild()`, `removeChild()`, and `replaceChild()` methods to add, delete, or modify elements on a webpage.

- Changing element attributes: You can use the `setAttribute()` and `removeAttribute()` methods to change the attributes of an element, or you can access the attributes directly using the attributes property of an element.

- Changing element styles: You can use the style property of an element to change its inline styles, or you can use the `className` property to change its class name and apply styles using CSS.

- Modifying text content: You can use the `textContent` property to change the text content of an element, or you can use the `innerHTML` property to change the HTML content of an element.

Here is an example of using the DOM to modify a webpage:

```javascript
const element = document.getElementById("myId");
element.innerHTML = "new content";
element.style.fontFamily = "Arial";
/* for css styles, instead of hyphens(-), we use camel case to represent styles with more than 1 word */
element.className = "new-class another-class";
```

#### Hacking with the DOM

Here are some common tactics used by hackers

- Injecting malicious code into a webpage: Hackers can use the DOM to inject malicious code into a webpage, which can be used to steal sensitive information or to perform other nefarious actions.

- Manipulating form inputs: Hackers can use the DOM to manipulate form inputs, such as changing the values of hidden fields or altering the behavior of submit buttons.

- Bypassing security measures: Hackers can use the DOM to bypass security measures, such as bypassing CAPTCHAs or disabling client-side form validation.

We will discuss strategies later and how too take advantage of these
