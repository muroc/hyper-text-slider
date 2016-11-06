# Utilizing [CSS3 Transitions](http://www.w3.org/TR/css3-transitions/)

[![Build Status](https://travis-ci.org/webfront-toolkit/hermes.svg?branch=master
)](https://travis-ci.org/webfront-toolkit/hermes)
[![Dependency Status](https://david-dm.org/webfront-toolkit/hermes.svg
)](https://david-dm.org/webfront-toolkit/hermes)
[![devDependency Status](https://david-dm.org/webfront-toolkit/hermes/dev-status.svg
)](https://david-dm.org/webfront-toolkit/hermes?type=dev)
[![Documentation Status](https://inch-ci.org/github/webfront-toolkit/hermes.svg?branch=master
)](https://inch-ci.org/github/webfront-toolkit/hermes)
[![Code Climate](https://codeclimate.com/github/webfront-toolkit/hermes/badges/gpa.svg
)](https://codeclimate.com/github/webfront-toolkit/hermes)

Hermes comes with:

 * configurable background and content transitions,
 * responsiveness (automatically adjusts it's layout to screen resolution),
 * extendability (adding new transtitions is very simple),
 * component-based approach (each feature can be enabled separately),
 * HTML/CSS programming interface (no JavaScript coding required).

## Getting the Code

Preferred way to get hermes is to use [bower](http://bower.io/).
```shell
bower install hermes --save-dev
```

You can also use [npm](https://www.npmjs.com/) (especially if using
[browserify](https://github.com/substack/node-browserify)).
```shell
npm install --save hermes-slider
```

## Hello, Hermes!

```html
<!DOCTYPE html>
<html>
<head>
  <title>Hello, Hermes!</title>

  <!--
    There are 4 things things needed for Hermes to work:

     1. Hermes' CSS (styles for the slider).
  -->
  <link href=bower_components/hermes/dist/hermes.min.css
        rel=stylesheet type=text/css>
</head>

<!--
     2. A flag on document's body which instructs Hermes to automatically
       create and start Slider objects for all declared sliders on the page
       (no JavaScript programming required).
-->
<body class="hermes-autoboot">

  <!--
     3. Declaration of a slider (features are enabled by adding class names
       to the slider element; this is a minimal configuration, but you can
       get pretty wild in here; please consult documentation for details).
  -->
  <div class="hermes-slider hermes-defaults">
    <div id=hello>
      <h1>Hello, Hermes!</h2>
    </div>
    <div id=transitions class=hermes-theme--black>
      <p>How's the waether?</p>
    </div>
  </div>

  <!--
     4. And Hermes script (it could be placed in the head section,
       but page may render a little faster this way).
  -->
  <script src=bower_components/hermes/dist/core.min.js type=text/javascript>
  </script>
</body>
</html>

```

## Documentation

API Reference:
 * [Declarative API](doc/class-names.md)
 * [JavaScript API](doc/javascript-api.md)

User Guides:
 * [Adding Custom Themes](doc/custom-themes.md)
 * [Screen Responsiveness](doc/responsiveness.md)
 * [Slider's DOM Upgrade](doc/dom-upgrade.md)

Tutorials:
 * [Hermes via Node and Browserify][hermes-node-example]

See Also:
 * [Animatable CSS Properties][animatable]

Project Info:
 * [TODO List](doc/TODO.md)
 * [CHANGELOG](doc/CHANGELOG.md)
 
[hermes-node-example]: https://github.com/webfront-toolkit/hermes-node-example
[animatable]: https://drafts.csswg.org/css-transitions/#animatable-properties

## Contributing

Please read [build.config.js](build.config.js) file before contributing. Pull
requests are very welcome!

## License

Copyright &copy; 2016 Maciej Chałapuk. Released under [Apache License Version 2.0](LICENSE).

