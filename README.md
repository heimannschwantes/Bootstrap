24.11.17
# Bootstrap documentation :thumbsup:
aktuelle Version: v4.0.0-beta.2

## Starter template

most basic html structure

```html
<!doctype html>
<html lang="en">
  <head>
    <title>Hello, world!</title>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" integrity="sha384-PsH8R72JQ3SOdhVi3uxftmaW6Vc51MKb0q5P2rRUpPvrszuE4W1povHYgTpBfshb" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.3/umd/popper.min.js" integrity="sha384-vFJXuSJphROIrBnz7yo7oB41mKfc8JzQZiCq4NCceLEaO4IHwicKwpJf9c9IpFgh" crossorigin="anonymous"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/js/bootstrap.min.js" integrity="sha384-alpBpkh1PFOepccYVYDB4do5UnbKysX5WZXm3XxPqe5iKTfUKjNkCk9SaVuEZflJ" crossorigin="anonymous"></script>
  </body>
</html>
```

[Source](https://getbootstrap.com/docs/4.0/getting-started/introduction/#starter-template)

## Grid System

### Container

the bootstrap grid system requires any of the two (.container / .container-fluid) container-classes.

```html
<div class="container">
  <!-- Content here -->
</div>
```
fixed-width container (meaning its max-width changes at each breakpoint)

```html
<div class="container-fluid">
  <!-- Content here -->
</div>
```
 fluid-width (meaning it’s 100% wide all the time)
 
[Source](https://getbootstrap.com/docs/4.0/layout/overview/#containers)

### Breakpoints
```css
// Extra small devices (portrait phones, less than 576px)
// No media query since this is the default in Bootstrap

// Small devices (landscape phones, 576px and up)
@media (min-width: 576px) { ... }

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) { ... }

// Large devices (desktops, 992px and up)
@media (min-width: 992px) { ... }

// Extra large devices (large desktops, 1200px and up)
@media (min-width: 1200px) { ... }
```
[Source](https://getbootstrap.com/docs/4.0/layout/overview/#responsive-breakpoints)

   | Extra small  | Small   | Medium
   | <576px	      | ≥576px  | ≥768px
   |
	
	Large
≥992px	Extra large
≥1200px
Max container width	None (auto)	540px	720px	960px	1140px
Class prefix	.col-	.col-sm-	.col-md-	.col-lg-	.col-xl-
# of columns	12
Gutter width	30px (15px on each side of a column)
Nestable	Yes
Column ordering	Yes



![logo](https://github.com/heimannschwantes/Bootstrap/blob/master/ADK_archiv_logo_sm.jpg)
