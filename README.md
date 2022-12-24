# JavaScript Hacking: A comprehensible guide

JavaScript is a powerful and versatile programming language that is widely used on the web for various purposes, such as validating form input, creating interactive content, and tracking user behavior. However, JavaScript can also be used by attackers to compromise the security of a website or web application.

## What we'll cover:

- DOM
- API's
- Sessions & Cookies
- Security Protocols
- Encryption
- Strategies

### The Document Object Model (DOM)

The Document Object Model (DOM) is a tree-like structure that represents the content and layout of a webpage. It allows developers to manipulate the content and styling of a webpage using JavaScript.

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

| Node | Description |
| ----------- | ----------- |
| Document  | The root node of the DOM, representing the entire document. |
| Element   | A node that represents an HTML element, such as a `div`, `p`, or `a`. |
| Attribute | A node that represents an attribute of an HTML element, such as the `src` attribute of an `img` element.  Typically displayed as `<element attribute="value">` |
| Text      | A node that represents the text content of an element. Defined as `<element>text content</element> |

Each node in the DOM has properties and methods that can be accessed and manipulated using JavaScript. Here is a table of some common properties and methods for DOM nodes:

| Node
