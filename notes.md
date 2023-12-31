# Web Programming Notes
Git commands I've Learned and how I currently understand them

- `git status`: checks if my repsoitory is current on my device and online
- `git add`: Adds any new directories to the repository?
- `git commit`: Commits my changes to the repository to check to see if there are any conflicts
- `git push`: actually makes the changes to the repository
- `git pull`: gets any changes that were made somewhere else onto the device

## HTML

### Basic HTML Document Structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
    <link rel="stylesheet" href="styles.css">
    <script src="script.js"></script>
</head>
<body>
    <h1>Welcome to My Page</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

### Common HTML Tags:

- **Headings**: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
- **Paragraph**: `<p>`
- **Links**: 
  ```html
  <a href="https://example.com">Visit Example.com</a>
  ```
- **Images**: 
  ```html
  <img src="image-path.jpg" alt="Image description">
  ```
- **Lists**: 
  ```html
  <ul>
      <li>List item 1</li>
      <li>List item 2</li>
  </ul>
  
  <ol>
      <li>First item</li>
      <li>Second item</li>
  </ol>
  ```
### Link Tags:

```html
<!-- Internal link -->
<a href="/about.html">About Us</a>

<!-- External link -->
<a href="https://example.com">Visit Example.com</a>

<!-- Open in a new tab/window -->
<a href="https://example.com" target="_blank">Open in New Tab</a>
```

### Div Tags:

```html
<!-- The 'div' element is a container that can be used to group content -->
<div>
    <p>This is inside the div.</p>
</div>
```

## CSS

### Basic Styling:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
}

h1 {
    color: #333;
}

p {
    font-size: 16px;
}
```

### Styling with Classes and IDs:

```css
/* By Class */
.button {
    padding: 10px 15px;
    background-color: blue;
    color: white;
}

/* By ID */
#specialText {
    font-weight: bold;
}
```

### Combining Selectors:

```css
/* Styling anchor tags within a specific class */
.navbar a {
    text-decoration: none;
}

/* Styling paragraphs that are directly after an h1 */
h1 + p {
    font-style: italic;
}
```

### Padding and Margin:

- **Padding**: Space _inside_ an element's boundary.
- **Margin**: Space _outside_ an element's boundary.

```css
/* Example with padding and margin */
.box {
    padding: 20px; /* Space inside the box */
    margin: 30px;  /* Space outside the box */
}
```

### Flexbox:

Flexbox is a layout model that allows items in a container to be dynamically arranged based on certain properties.

```css
.container {
    display: flex; /* This activates the Flexbox layout */
    justify-content: space-between; /* Distributes items evenly across the container */
}

.item {
    flex: 1; /* Each item will take up equal width inside the container */
}
```

## JavaScript

### Basic Syntax:

```javascript
let variableName = "This is a variable";
const CONSTANT_NAME = "This is a constant";

function functionName() {
    console.log("Function called");
}

// This is a comment
/* This is a multi-line
   comment */
```

### Variables, Functions, Classes, and Objects:

```javascript
// Variables
let name = "John";

// Functions
function greet(person) {
    console.log("Hello, " + person + "!");
}

// Classes
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    sayHello() {
        console.log("Hello, my name is " + this.name);
    }
}

// Objects
let person1 = new Person("Jane", 30);
person1.sayHello();
```

### Promises, Async, and Await:

```javascript
// Promises
let myPromise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("Promise resolved");
    }, 1000);
});

myPromise.then(result => {
    console.log(result);
});

// Async & Await
async function fetchData() {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();
    console.log(data);
}
```

### Accessing the DOM:

```javascript
// Selecting an element by ID
let element = document.getElementById("myElement");

// Changing the text of an element
element.innerText = "New text content";

// Adding an event listener
element.addEventListener("click", function() {
    alert("Element was clicked!");
});
```

`<a href="https://example.com" target="_blank">Open in New Tab</a>`
```

### Div Tags:

```html
<!-- The 'div' element is a container that can be used to group content -->
<div>
    <p>This is inside the div.</p>
</div>
```

### Arrow Functions:

```javascript
// Traditional function
function add(a, b) {
    return a + b;
}

// Arrow function equivalent
const add = (a, b) => a + b;
```

### Data Structures:

- **Arrays** - List-like objects that allow you to store multiple values in a single variable.
  
  ```javascript
  let fruits = ["apple", "banana", "cherry"];
  ```

- **Maps** - A collection of key-value pairs. Any value (both objects and primitive values) may be used as either a key or a value.

  ```javascript
  let myMap = new Map();
  myMap.set("name", "John");
  ```

  ### Basic Facts about the DOM:

- **DOM** stands for **Document Object Model**.
- It represents the structure of an HTML document.
- With the DOM, JavaScript can access and change HTML elements, attributes, and content.

### JSON in JavaScript:

**JSON** (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write. 

```javascript
// JavaScript object
let person = {
    name: "John",
    age: 30
};

// Convert to JSON string
let jsonString = JSON.stringify(person);

// Convert JSON string back to JavaScript object
let jsonObject = JSON.parse(jsonString);
```

## Console

### Remote Shell Sessions:

You can use the `ssh` command to create remote shell sessions:

```bash
ssh username@remotehost.com
```

### `-la` Parameter and Other Common Parameters:

- `ls -la`: List all (`-a`) files including the hidden ones in long (`-l`) format.
- `-l`: Displays files in long format.
- `-a`: Includes directory entries whose names begin with a dot (`.`).

### Difference between Top Level Domain, Subdomain, and Root Domain:

- **Top Level Domain (TLD)**: The last segment of the domain name. Examples: `.com`, `.org`, `.net`.
- **Subdomain**: A domain that is part of a larger domain. For example, in `blog.example.com`, `blog` is a subdomain.
- **Root Domain**: The combination of the domain name and the TLD. For example, in `www.example.com`, `example.com` is the root domain.

## Example problems

1. **By default, the HTML span element has a default CSS display property value of:** 
   - `inline`.

2. **How would you use CSS to change all the div elements to have a background color of red?**
   ```css
   div {
       background-color: red;
   }
   ```

3. **How would you display an image with a hyperlink in HTML?**
   ```html
   <a href="https://example.com">
       <img src="path-to-image.jpg" alt="Description of image">
   </a>
   ```

4. **In the CSS box model, what is the ordering of the box layers starting at the inside and working out?**
   - Content, Padding, Border, Margin.

5. **How would you use JavaScript to select an element with the id of “byu” and change the text color of that element to green?**
   ```javascript
   document.getElementById("byu").style.color = "green";
   ```

6. **What is the opening HTML tag for a paragraph, ordered list, unordered list, second level heading, first level heading, third level heading?**
   - Paragraph: `<p>`
   - Ordered list: `<ol>`
   - Unordered list: `<ul>`
   - Second level heading: `<h2>`
   - First level heading: `<h1>`
   - Third level heading: `<h3>`

7. **How do you declare the document type to be html?**
   ```html
   <!DOCTYPE html>
   ```

8. **What is valid JavaScript syntax for if, else, for, while, switch statements?**
   ```javascript
   if (condition) {
       // code
   } else {
       // code
   }

   for (let i = 0; i < 10; i++) {
       // code
   }

   while (condition) {
       // code
   }

   switch(expression) {
       case value1:
           // code
           break;
       case value2:
           // code
           break;
       default:
           // code
   }
   ```

9. **What is the correct syntax for creating a JavaScript object?**
   ```javascript
   let objectName = {
       key1: 'value1',
       key2: 'value2'
   };
   ```

10. **Is it possible to add new properties to JavaScript objects?**
   - Yes, it is possible. For example:
     ```javascript
     objectName.newProperty = 'newValue';
     ```

11. **If you want to include JavaScript on an HTML page, which tag do you use?**
   ```html
   <script src="path-to-javascript-file.js"></script>
   ```

12. **Console commands and their functionalities:**
   - `chmod`: Changes the permissions of a file.
   - `pwd`: Prints the current working directory.
   - `cd`: Changes the current directory.
   - `ls`: Lists the files in the current directory.
   - `vim`: Opens the VIM text editor.
   - `nano`: Opens the nano text editor.
   - `mkdir`: Creates a new directory.
   - `mv`: Moves or renames files or directories.
   - `rm`: Removes files or directories.
   - `man`: Displays the manual page for a command.
   - `ssh`: Connects to a remote server over SSH.
   - `ps`: Displays a list of currently running processes.
   - `wget`: Downloads files from the internet.
   - `sudo`: Runs a command with superuser permissions.

13. **Is a web certificate necessary to use HTTPS?**
   - Yes, an SSL/TLS certificate is necessary to establish a secure HTTPS connection.

14. **Port numbers and their associated protocols:**
   - Port 443: HTTPS
   - Port 80: HTTP
   - Port 22: SSH

# **Final Review**

1. **What ports are used for HTTP, HTTPS, SSH?**
   - HTTP typically uses port 80, HTTPS uses port 443, and SSH uses port 22.

2. **What do HTTP status codes in the 300, 400, 500 range indicate?**
   - 300 range status codes indicate redirections, 400 range indicate client errors, and 500 range indicate server errors.

3. **What does the HTTP header content-type allow you to do?**
   - The "Content-Type" HTTP header specifies the media type of the resource, helping the client process the received data correctly.

4. **What do the following attributes of a cookie do? Domain, Path, SameSite, HTTPOnly?**
   - **Domain**: Specifies which domain the cookie is accessible to.
   - **Path**: Restricts the cookie to a specific path within the domain.
   - **SameSite**: Controls the cookie's sending along with cross-origin requests.
   - **HTTPOnly**: Makes the cookie accessible only through the HTTP protocol.

5. **Assuming the following Express middleware, what would be the console.log output for an HTTP GET request with a URL path of /foo/bar?**
   Here's the middleware:
   ```javascript
   app.use((req, res, next) => {
     console.log(req.method, req.path);
     next();
   });
   ```
   - The output for a GET request to `/foo/bar` would be: `GET /foo/bar`.

6. **Given the following Express service code: What does the following JavaScript fetch return?**
   - Generally, `fetch()` returns a Promise resolving to the Response of the request.

7. **Given the following MongoDB query { cost: { $gt: 10 }, name: /fran.*/ } select all of the matching documents.**
   - This query selects documents where `cost` is greater than 10 and `name` starts with "fran".

8. **How should you store user passwords in a database?**
   - User passwords should be stored in hashed form using algorithms like bcrypt, with salts for added security.

9. **Assuming the following Node.js service code is executing with websockets, what will be logged to the console of the web browser?**
   - Generally, WebSocket interactions can send messages to the client to be logged in the browser.

10. **What is the WebSocket protocol used for?**
    - The WebSocket protocol is for two-way interactive communication between a user's browser and a server.

11. **What is JSX and how are the curly braces rendered?**
    - JSX is a syntax extension for JavaScript, used in React. Curly braces in JSX embed JavaScript expressions in the markup.

12. **Assuming a HTML document with a `<div id="root"></div>` element, what content will the following React component generate?**
    The React component provided:
    ```javascript
    function Welcome(props) {
      return <h1>Hello, {props.name}</h1>;
    }
    function App() {
      return (
        <div>
          <Welcome name="Sara" />
          <Welcome name="Cahal" />
          <Welcome name="Edite" />
        </div>
      );
    }
    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<App />);
    ```
    This will generate:
    ```html
    <div>
      <h1>Hello, Sara</h1>
      <h1>Hello, Cahal</h1>
      <h1>Hello, Edite</h1>
    </div>
    ```

13. **Assuming a HTML document with a `<div id="root"></div>` element, what content will the following React component generate?**
    The `Numbers` component:
    ```javascript
    function Numbers() { 
      const numbers = [1, 2, 3, 4, 5];
      const listItems = numbers.map((number) =>
        <li>{number}</li>
      );
      return(<ul>{listItems}</ul>)
    }
    const root = ReactDOM.createRoot(document.getElementById('root')); 
    root.render(<Numbers/>);
    ```
    - This generates an unordered list with numbers 1 to 5 as list items.

14. **What does the following React component do?**
    The `Example` component:
    ```javascript
    function Example() {
      const [count, setCount] = useState(0);
      return (
        <div>
          <p>You clicked {count} times</p>
          <button onClick={() => setCount(count + 1)}>
            Click me
          </button>
        </div>
      );
    }
    ```
    It's a counter component that increments the count each time the button is clicked.

15. **What are React Hooks used for?**
    - React Hooks allow function components to use React state and lifecycle features.

16. **What is the useEffect hook used for?**
    - `useEffect` is for performing side effects in function components, like data fetching or manual DOM changes.

17. **What does this code do?**
    The provided code:
    ```javascript
    export default function App() {
      return (
        <BrowserRouter>
          <Routes>
            <Route path="/" element={<Layout />}>
              <Route index element={<Home />} />
              <Route path="blogs" element={<Blogs />} />
              <Route path="contact" element={<Contact />} />
              <Route path="*" element={<NoPage />} />
            </Route>
          </Routes>
        </BrowserRouter>
      );
    }
    ```
    - It sets up a router in a React application, defining routes for different components.

18. **What role does npm play in web development?**
    - npm is a package manager for JavaScript, used for installing, sharing, and managing project dependencies.

19. **What does package.json do in an npm project?**
    - `package.json` holds project metadata and manages project dependencies, scripts, and versions.

20. **What does the fetch function do?**
    - `fetch` makes network requests and returns a Promise resolving to the Response of the request.

21. **What does Node.js do?**
    - Node.js is a JavaScript runtime for server-side and networking applications.

22. **What does Vite do?**
    - Vite is a front-end build tool for faster server start, instant module reloading, and efficient bundling.
