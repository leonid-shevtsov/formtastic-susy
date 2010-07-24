# Formtastic Susy

I've used Formtastic for quite some time. Now I met Susy. Susy was good, but not quite formtastic, so I teached her a few things myself.

## More prosaic

This is a port of the original Formtastic stylesheet (that I happen to like) to the [Susy](http://susy.oddbird.net) framework, based on [Compass](http://compass-style.org), based on [Sass](http://sass-lang.com). I suppose you know what those are.

See `demo/formtastic.html` if you're not convinced.

## Installation & Usage

Formtastic Susy depends on Susy and Compass.

Just drop `_formtastic.scss` into your Sass stylesheet directory and include it in your `screen.scss` or anywhere else.

## Differences from vanilla Formtastic

The default Formtastic Susy styles (included in `form.formtastic`) expect a 12-column form. The original Formtastic styles are scalable (though that is debatable).

I also tried to preserve vertical rhythm as much as possible (I'm a coder, you know). That required the `textarea` to be of a known size in rows.

## Customization

There are some relevant variables in `_formtastic.scss`, hopely self-documentable.

## TODO

* Test, test, test.
* Make it possible to set up custom form width.
