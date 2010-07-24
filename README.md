# Formtastic Susy

I've known Formtastic for quite some time. Now I met Susy. Susy was good, but not quite formtastic, so I teached her a few things myself.

## More prosaic

This is a port of the original [Formtastic](http://github.com/justinfrench/formtastic) stylesheet (that I happen to like) to the [Susy](http://susy.oddbird.net) framework, based on [Compass](http://compass-style.org), based on [Sass](http://sass-lang.com). I suppose you know what those are.

See `demo/formtastic.html` if you're not convinced.

## Installation & Usage

Formtastic Susy depends on Susy and Compass.

Drop `_formtastic.scss` into your Sass stylesheet directory. Then, include it in your `screen.scss` or anywhere else:

    @import "formtastic"
    form.formtastic {
      @include formtastic;
    }

The `formtastic` helper accepts three parameters:

* label width in columns;
* input "area" width in columns;
* current context (if it's different from the main context)

For example, if your form is in a 8-column wide `.content` block and you want to have 50-50 space for labels and inputs, use

    .content form.formtastic {
      @include formtastic(4,4,8);
    }

## Differences from vanilla Formtastic

The vanilla Formtastic form was scalable context-independently. That doesn't play well with grids. Formtastic Susy uses the grid provided
by Susy via its mixins - that's why the form fits any grid you happen to use.

I also tried to preserve vertical rhythm as much as possible (I'm a coder, you know). That required the `textarea` to be of a known size 
in rows. I haven't yet found a way to simplify this.

## Customization

There are some relevant variables in `_formtastic.scss`, hopely self-documentable.

## TODO

* Test, test, test.
  * `ul.errors` are hardly tested
  * `input` paddings break the grid if the grid is too narrow
* Maybe divide into separate helpers for paddings, error messages, etc. I don't think this is useful.

* * *

This port was made by Leonid Shevtsov from the original Formtastic stylesheet prepared by Justin French.
