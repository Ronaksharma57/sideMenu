## Tech Fanatic

### Step 1: Create a New HTML File

Create a new file called `index.html` and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tech-Fanatic</title>

    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"
      integrity="sha512-z3gLpd7yknf1YoNbCzqRKc4qyor8gaKU1qmn+CShxbuBusANI9QpRohGBreCFkKxLhei6S9CQXFEbbKuqLg0DA=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <i class="fa fa-bars" aria-hidden="true"></i>

    <div class="sidebar">
      <div class="sidebar-header">
        <p class="logo">@Tech-Fanatic</p>
        <i class="fa fa-times" aria-hidden="true"></i>
      </div>
      <ul class="menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
    <script src="index.js"></script>
  </body>
</html>
```

### Step 2: Create a New CSS File

Create a new file called `style.css` and add the following code:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  background: #ebebeb;
}

.menu a {
  display: block;
  font-size: 1.5rem;
  padding: 1rem 1.5rem;
  color: grey;
  transition: all 0.3s linear;
  text-decoration: none;
}

.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  background: white;
  width: 100%;
  height: 100%;
  transition: all 0.3s linear;
  transform: translate(-100%);
}

.show-sidebar {
  transform: translate(0);
}

.fa-bars {
  position: fixed;
  top: 2rem;
  right: 3rem;
  color: #e94949;
  font-size: 1.5rem;
  cursor: pointer;
}

.fa-bars:hover {
  color: black;
}

.fa-times {
  font-size: 1.5rem;
  color: #e94949;
  cursor: pointer;
}

.fa-times:hover {
  color: black;
}

.sidebar-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 1.5rem;
}

.logo {
  font-weight: 900;
  font-size: 30px;
  color: rgb(241, 188, 12);
}

@media (min-width: 676px) {
  .sidebar {
    width: 500px;
  }
}

.menu a:hover {
  background: #f8a5a5;
  padding-left: 1.7rem;
}
```

### Step 3: Create a New CSS File

Create a new file called `index.js` and add the following code:

```js
const bars = document.querySelector(".fa-bars");
const sidebar = document.querySelector(".sidebar");
const closingButton = document.querySelector(".fa-times");

bars.addEventListener("click", () => {
  sidebar.classList.toggle("show-sidebar");
});

closingButton.addEventListener("click", () => {
  sidebar.classList.remove("show-sidebar");
});
```
