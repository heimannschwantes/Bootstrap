24.11.17
# Bootstrap documentation :thumbsup: 
aktuelle Version: v4.0.0-beta.2


## Starter template

html base structure

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
Source: https://getbootstrap.com/docs/4.0/getting-started/introduction/#starter-template

#### :point_right: [Codepen B4 Setup Template](https://codepen.io/heimannschwantes/pen/qVKxme)


## Grid System

Links for more information:
- https://getbootstrap.com/docs/4.0/layout/grid/
- https://www.w3schools.com/bootstrap4/bootstrap_grid_system.asp

### Container > Row > Column

#### Container

the bootstrap grid system requires any of the two (`.container` / `.container-fluid`) container-classes.

```html
<div class="container">
  <!-- Content here -->
</div>
```
- fixed-width container (meaning its max-width changes at each breakpoint)

```html
<div class="container-fluid">
  <!-- Content here -->
</div>
```
- fluid-width (meaning it’s 100% wide all the time)
 
Source: https://getbootstrap.com/docs/4.0/layout/overview/#containers
#### :point_right: [Codepen B4 Container](https://codepen.io/heimannschwantes/pen/pdKVrN?#)

#### Row
- In the grid layout, content must be placed within columns and only columns may be immediate children of rows
  - `.container` (or `.container-fluid`) = wrapper for `.row`
  - `.row` = wrapper for `.col`

#### Column

- max. 12 columns per row
- Since v4 the bootstrap grid system is built with flexbox grid columns without a specified width will automatically layout as equal width columns (flexbox behaviour
- See also. [CSS-Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#flexbox-background)

#### basic example (Container > Row > Column)
- 2 `.row`s; 1st `.row` with 2 `.col`s, 2nd row with 3 `.col`s. All `.col`s have an equal with within their `.row` since there is no width specified
```html
<div class="container">
  <div class="row">
    <div class="col">
      1 of 2
    </div>
    <div class="col">
      2 of 2
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col">
      2 of 3
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
</div>
```
Source: https://getbootstrap.com/docs/4.0/layout/grid/#equal-width

#### :point_right: [Codepen B4 Grid 1–12 Columns](https://codepen.io/heimannschwantes/pen/POaeBw)

```html
<!-- Let Bootstrap automatically handle the layout -->
<div class="row">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>

<!-- Or Control the column width, and how they should appear on different devices -->
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
```
Source: https://www.w3schools.com/bootstrap4/bootstrap_grid_system.asp


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
Source: https://getbootstrap.com/docs/4.0/layout/overview/#responsive-breakpoints


### Grid Classes and Options
- `.col-` (extra small devices - screen width less than 576px)
- `.col-sm-` (small devices - screen width equal to or greater than 576px)
- `.col-md-` (medium devices - screen width equal to or greater than 768px)
- `.col-lg-` (large devices - screen width equal to or greater than 992px)
- `.col-xl-` (xlarge devices - screen width equal to or greater than 1200px)

![bootstrap grid options](https://github.com/heimannschwantes/Bootstrap-documentation/blob/master/Bildschirmfoto%202017-11-22%20um%2010.46.52.png)\
Source: https://getbootstrap.com/docs/4.0/layout/grid/#grid-options

![bootstrap grid options](https://github.com/heimannschwantes/Bootstrap-documentation/blob/master/Bildschirmfoto%202017-11-24%20um%2011.47.50.png)
Source: https://www.w3schools.com/bootstrap4/bootstrap_grid_system.asp

#### :point_right: [Codepen column widths and responsive behaviour](https://codepen.io/heimannschwantes/pen/wPXXwz)


### Vertical alignment

See: https://getbootstrap.com/docs/4.0/layout/grid/#alignment

```html
<div class="container">
  <div class="row align-items-start">
    <div class="col col-3">.col</div>
    <div class="col col-6">.col</div>
    <div class="col col-3">.col</div>
  </div>
  <div class="row align-items-center">
    <div class="col col-4">.col</div>
    <div class="col col-4">.col</div>
    <div class="col col-4">.col</div>
  </div>
  <div class="row align-items-end">
    <div class="col col-2">.col</div>
    <div class="col col-8">.col</div>
    <div class="col col-2">.col</div>
  </div>
</div>
```

#### :point_right: [Codepen vertical alignment](https://codepen.io/heimannschwantes/pen/ooyEyj)

## Typography
- https://getbootstrap.com/docs/4.0/content/typography/
- https://www.w3schools.com/bootstrap4/bootstrap_typography.asp
- Background and Text Colors: https://www.w3schools.com/bootstrap4/bootstrap_colors.asp

## Images
- https://getbootstrap.com/docs/4.0/content/images/
- https://www.w3schools.com/bootstrap4/bootstrap_images.asp

## Tables
- https://getbootstrap.com/docs/4.0/content/tables/
- https://www.w3schools.com/bootstrap4/bootstrap_tables.asp

## Components
- https://getbootstrap.com/docs/4.0/components/
- See also here: https://www.w3schools.com/bootstrap4/


## Link List

##### B4 Documentation – getbootstrap
- https://getbootstrap.com/docs/4.0/getting-started/introduction/

##### B4 Tutorial – W3Schools
- https://www.w3schools.com/bootstrap4/

##### Bootstrap 4 Cheat Sheet
- https://hackerthemes.com/bootstrap-cheatsheet/
  
##### CSS-Tricks Flexbox Guide
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/#flexbox-background
