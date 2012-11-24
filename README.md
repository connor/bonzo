## Bonzo

Bonzo is a library-agnostic, extensible DOM utility. Nothing else.

It's designed to live in any host library, or simply as a stand-alone tool for the majority of your DOM-related tasks.

### Examples

``` js
bonzo(elements)
  .hide()
  .addClass('foo')
  .append('<p>the happs</p>')
  .css({
    color: 'red',
    'background-color': 'white'
  })
  .show()
```

## Paired with a Selector Engine

A great way to use Bonzo is with a selector engine (like [Qwery](https://github.com/ded/qwery) for example). You could wrap bonzo up and augment your wrapper to inherit the same methods. That looks like this:

``` js
function $(selector) {
  return bonzo(qwery(selector));
}
```

This now allows you to write the following code:

``` js
$('#content a[rel~="bookmark"]').after('√').css('text-decoration', 'none');
```

## Bonzo Extension API

One of the greatest parts about Bonzo is its simplicity to hook into the internal chain to create custom methods. For example, you can create a method called **color** like this:

``` js
bonzo.aug({
  color: function (c) {
    return this.css('color', c);
  }
})

// you can now do the following
$('p').color('aqua')
```

## API

* <a href="#each"><code>bonzo<b>.each(callback)</b></code></a>
* <a href="#map"><code>bonzo<b>.map(callback, rejext)</b></code></a>
* <a href="#html"><code>bonzo<b>.html()</b></code></a>
* <a href="#text"><code>bonzo<b>.text()</b></code></a>
* <a href="#addclass"><code>bonzo<b>.addClass()</b></code></a>
* <a href="#removeclass"><code>bonzo<b>.removeClass()</b></code></a>
* <a href="#hasclass"><code>bonzo<b>.hadClass()</b></code></a>
* <a href="#toggleclass"><code>bonzo<b>.toggleClass()</b></code></a>
* <a href="#show"><code>bonzo<b>.show()</b></code></a>
* <a href="#hide"><code>bonzo<b>.hide()</b></code></a>
* <a href="#first"><code>bonzo<b>.first()</b></code></a>
* <a href="#last"><code>bonzo<b>.last()</b></code></a>
* <a href="#focus"><code>bonzo<b>.focus()</b></code></a>
* <a href="#blur"><code>bonzo<b>.blur()</b></code></a>
* <a href="#next"><code>bonzo<b>.next()</b></code></a>
* <a href="#previous"><code>bonzo<b>.previous()</b></code></a>
* <a href="#parent"><code>bonzo<b>.parent()</b></code></a>
* <a href="#append"><code>bonzo<b>.append()</b></code></a>
* <a href="#appendto"><code>bonzo<b>.appendTo()</b></code></a>
* <a href="#prepend"><code>bonzo<b>.prepend()</b></code></a>
* <a href="#prependTo"><code>bonzo<b>.prependTo()</b></code></a>
* <a href="#before"><code>bonzo<b>.before()</b></code></a>
* <a href="#insertBefore"><code>bonzo<b>.insertBefore()</b></code></a>
* <a href="#after"><code>bonzo<b>.after()</b></code></a>
* <a href="#after"><code>bonzo<b>.insertAfter()</b></code></a>
* <a href="#replacewith"><code>bonzo<b>.replaceWith()</b></code></a>
* <a href="#css"><code>bonzo<b>.css()</b></code></a>
* <a href="#offset"><code>bonzo<b>.offset()</b></code></a>
* <a href="#dim"><code>bonzo<b>.dim()</b></code></a>
* <a href="#attr"><code>bonzo<b>.attr()</b></code></a>
* <a href="#removeattr"><code>bonzo<b>.removeattr()</b></code></a>
* <a href="#val"><code>bonzo<b>.val()</b></code></a>
* <a href="#data"><code>bonzo<b>.data()</b></code></a>
* <a href="#remove"><code>bonzo<b>.remove()</b></code></a>
* <a href="#empty"><code>bonzo<b>.empty()</b></code></a>
* <a href="#detach"><code>bonzo<b>.detach()</b></code></a>
* <a href="#scrollleft"><code>bonzo<b>.scrollLeft()</b></code></a>
* <a href="#scrolltop"><code>bonzo<b>.scrollTop()</b></code></a>
* <a href="#aug"><code>bonzo<b>.aug()</b></code></a>
* <a href="#doc"><code>bonzo<b>.doc()</b></code></a>
* <a href="#viewport"><code>bonzo<b>.viewport()</b></code></a>
* <a href="#isancestor"><code>bonzo<b>.isAncestor()</b></code></a>
* <a href="#noconflict"><code>bonzo<b>.noConflict()</b></code></a>

## Added in the Ender bridge

  * parents(selector)
  * closest(selector)
  * siblings()
  * children()
  * width()
  * height()

## Setting a query engine host

For the insertion methods you can set a query selector host (like [qwery](https://github.com/ded/qwery)).

``` js
bonzo.setQueryEngine(qwery)
bonzo(bonzo.create('<div>')).insertAfter('.boosh a')
```

## The name Bonzo

Bonzo Madrid was a malicious battle school commander of whom eventually is killed by [Ender Wiggin](http://en.wikipedia.org/wiki/Ender_Wiggin). Bonzo represents the DOM, of whom we'd all love to slay.

## Building

    $ npm install -d
    $ make

## Tests

    $ open tests/tests.html

## Browser support

  * IE6+
  * Chrome
  * Safari 4+
  * Firefox 3+
  * Opera

## Ender integration

Bonzo is a registered npm package and fits in nicely with the [Ender](http://ender.no.de) framework. If you don't have Ender, you should install now, and never look back, ever. As a side note the *query engine host* is set for you when you include it with Ender.

    $ npm install ender -g

To combine Bonzo to your Ender build, you can add it as such:

    $ ender build bonzo[,modb, modc,...]

or, add it to your existing ender package

    $ ender add bonzo

## Contributors

  * [Dustin Diaz](https://github.com/ded/bonzo/commits/master?author=ded)
  * [Rod Vagg](https://github.com/ded/bonzo/commits/master?author=rvagg)
  * [Jacob Thornton](https://github.com/ded/bonzo/commits/master?author=fat)
