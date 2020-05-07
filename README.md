# Project 0

Web Programming with Python and JavaScript

# HTML

### index.html
- We using nav bar component from bootstrap and edit the entries of that component

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">Project0</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="index.html">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="about.html">About</a>
      </li>
      <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          Dropdown
        </a>
        <div class="dropdown-menu" aria-labelledby="navbarDropdown">
          <a class="dropdown-item" href="#">Action</a>
          <a class="dropdown-item" href="#">Another action</a>
          <div class="dropdown-divider"></div>
          <a class="dropdown-item" href="#">Something else here</a>
        </div>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
      </li>
    </ul>
  </div>
</nav>
```

- using grid system to display three responsive boxes

```bootstrap grid system
 <!--BootStrap Grid System-->
 <div class="container">
  <div class="row">
    <div class="col-lg-4 item-1">Column left</div>
    <div class="col-lg-4 item-2">Column middle</div>
    <div class="col-lg-4 item-2">Column right</div>
</div>
  
</div>
```
- An unordered list to display links to other four html pages we created

```html
 <ul>
      <li><a href="about.html">About</a></li>
      <li><a href="other.html">Other</a></li>
      <li><a href="contact.html">Contact</a></li>
      <li><a href="thanks.html">Thank You</a></li>
    </ul
```

- A table using bootstrap grid system to responsively display table data

```html
<table class="col-lg-4 col-sm-1 table">
    <tr>
      <th>countries</th>
      <th>Gross Domestic Product</th>
      <th>size rank</th>
    </tr>
    <tr>
      <td>india</td>
      <td>3 trillion usd</td>
      <td>4th</td>
    </tr>
    <tr>
      <td>UK</td>
      <td>2 trillion usd</td>
      <td>6th</td>
    </tr>
    <tr>
      <td>US</td>
      <td>20 trillion usd</td>
      <td>1st</td>
    </tr>
</table>
```

- Displaying image using img src

```html
<img src="ave-calvar-Q3gidZ3ZM5Y-unsplash.jpg" style="width:400px; height:400px" alt="Image Not Found" class="col-lg-4 col-sm-1">
```

# SCSS

```scss
$color: orange;

@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
@media only screen and (min-width: 600px) {
  body {
    background-color: lightgoldenrodyellow;
  }
}


%reuse {
  font-family: sans-serif;
  font-size: 18px;
  padding: 20px;
  margin: 20px;
}

.table{
  @extend %reuse;
  row-gap: 20px;
  column-gap: 20px;
}

.item-1{
  margin-bottom: 5px;
  margin-top: 5px;
  border: 1px solid $color;
}

.item-2{
  margin-bottom: 5px;
  margin-top: 5px;
  border: 1px solid blue;
}

body {
  margin: 30px;
}

th, td{
  border: 1px solid red;
}
```

- %reuse is used to create a template that can be inherited(reused) by other classes

- table class inherits from reuse template, we also give it a row-gap and column-gap property to give the data inside table more breathing space.

```table scss
.table{
  @extend %reuse;
  row-gap: 20px;
  column-gap: 20px;
}
```
- We use media queries to change background colour based on display size

```scss
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
@media only screen and (min-width: 600px) {
  body {
    background-color: lightgoldenrodyellow;
  }
}
```

- Install rubyinstaller-devkit in windows
- then open cmd and run the below line

```
command line
gem install sass
```

- To convert scss to css run the below command

```command line
sass index.scss index.css
```

- To automate the above process run the command below
```command line
sass --watch index.scss
```
- we use id selector to make the home button in nav bar italic

```scss
#home{
  font-style: italic;
}
```


