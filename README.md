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
* <a href="#addClass"><code>bonzo<b>.addClass()</b></code></a>
* <a href="#removeClass"><code>bonzo<b>.removeClass()</b></code></a>
* <a href="#hasClass"><code>bonzo<b>.hadClass()</b></code></a>
* <a href="#toggleClass"><code>bonzo<b>.toggleClass()</b></code></a>
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
* <a href="#appendTo"><code>bonzo<b>.appendTo()</b></code></a>
* <a href="#prepend"><code>bonzo<b>.prepend()</b></code></a>
* <a href="#prependTo"><code>bonzo<b>.prependTo()</b></code></a>
* <a href="#before"><code>bonzo<b>.before()</b></code></a>
* <a href="#insertBefore"><code>bonzo<b>.insertBefore()</b></code></a>
* <a href="#after"><code>bonzo<b>.after()</b></code></a>
* <a href="#insertAfter"><code>bonzo<b>.insertAfter()</b></code></a>
* <a href="#replaceWith"><code>bonzo<b>.replaceWith()</b></code></a>
* <a href="#css"><code>bonzo<b>.css()</b></code></a>
* <a href="#offset"><code>bonzo<b>.offset()</b></code></a>
* <a href="#dim"><code>bonzo<b>.dim()</b></code></a>
* <a href="#attr"><code>bonzo<b>.attr()</b></code></a>
* <a href="#removeAttr"><code>bonzo<b>.removeAttr()</b></code></a>
* <a href="#val"><code>bonzo<b>.val()</b></code></a>
* <a href="#data"><code>bonzo<b>.data()</b></code></a>
* <a href="#remove"><code>bonzo<b>.remove()</b></code></a>
* <a href="#empty"><code>bonzo<b>.empty()</b></code></a>
* <a href="#detach"><code>bonzo<b>.detach()</b></code></a>
* <a href="#scrollLeft"><code>bonzo<b>.scrollLeft()</b></code></a>
* <a href="#scrollTop"><code>bonzo<b>.scrollTop()</b></code></a>
* <a href="#aug"><code>bonzo<b>.aug()</b></code></a>
* <a href="#doc"><code>bonzo<b>.doc()</b></code></a>
* <a href="#viewport"><code>bonzo<b>.viewport()</b></code></a>
* <a href="#isAncestor"><code>bonzo<b>.isAncestor()</b></code></a>
* <a href="#noConflict"><code>bonzo<b>.noConflict()</b></code></a>

---

<a name="each"></a>
### each(callback)

`bonzo.each()` TODO

<a name="map"></a>
### map(callback)

`bonzo.map()` TODO

<a name="html"></a>
### html([string])

`bonzo.html()` TODO

<a name="text"></a>
### text([string])

`bonzo.text()` TODO

<a name="addClass"></a>
### addClass(className)

`bonzo.addClass(className)` TODO

<a name="removeClass"></a>
### removeClass(className)

`bonzo.removeClass(className)` TODO

<a name="hasClass"></a>
### hasClass(className)

`bonzo.hasClass(className)` TODO

<a name="toggleClass"></a>
### toggleClass(className)

`bonzo.toggleClass(className)` TODO

<a name="show"></a>
### show()

`bonzo.show()` TODO

<a name="hide"></a>
### hide()

`bonzo.hide()` TODO

<a name="first"></a>
### first()

`bonzo.first()` TODO

<a name="last"></a>
### last()

`bonzo.last()` TODO

<a name="focus"></a>
### focus()

`bonzo.focus()` TODO

<a name="blur"></a>
### blur()

`bonzo.blur()` TODO

<a name="next"></a>
### next()

`bonzo.next()` TODO

<a name="previous"></a>
### previous()

`bonzo.previous()` TODO

<a name="parent"></a>
### parent()

`bonzo.parent()` TODO

<a name="append"></a>
### append(html || node)

`bonzo.append()` TODO

<a name="appendTo"></a>
### appendTo(target || selector)

`bonzo.appendTo()` TODO

<a name="prepend"></a>
### prepend(html || node)

`bonzo.prepend()` TODO

<a name="prependTo"></a>
### prependTo(target || selector)

`bonzo.prepend()` TODO

<a name="before"></a>
### before(html || node)

`bonzo.before()` TODO

<a name="insertBefore"></a>
### insertBefore(target || selector)

`bonzo.insertBefore()` TODO

<a name="after"></a>
### after(html || node)

`bonzo.after()` TODO

<a name="insertAfter"></a>
### insertAfter(target || selector)

`bonzo.insertAfter()` TODO

<a name="replaceWith"></a>
### replaceWith(html || node)

`bonzo.replaceWith()` TODO

<a name="css"></a>
### css()

`bonzo.css()` TODO

<a name="offset"></a>
### offset()

`bonzo.offset()` TODO

<a name="dim"></a>
### dim()

`bonzo.dim()` TODO

<a name="attr"></a>
### attr()

`bonzo.attr()` TODO

<a name="removeAttr"></a>
### removeAttr()

`bonzo.removeAttr()` TODO

<a name="val"></a>
### val()

`bonzo.val()` TODO

<a name="data"></a>
### data()

`bonzo.data()` TODO

<a name="remove"></a>
### remove()

`bonzo.remove()` TODO

<a name="empty"></a>
### empty()

`bonzo.empty()` TODO

<a name="detatch"></a>
### detatch()

`bonzo.detatch()` TODO

<a name="scrollLeft"></a>
### scrollLeft()

`bonzo.scrollLeft()` TODO

<a name="scrollTop"></a>
### scrollTop()

`bonzo.scrollTop()` TODO

<a name="aug"></a>
### aug()

`bonzo.aug()` TODO

<a name="viewport"></a>
### viewport()

`bonzo.viewport()` TODO

<a name="isAncestor"></a>
### isAncestor()

`bonzo.isAncestor()` TODO

<a name="noConflict"></a>
### noConflict()

`bonzo.noConflict()` TODO



## Added in the Ender bridge

* <a href="#parents"><code>bonzo<b>.parents()</b></code></a>
* <a href="#closest"><code>bonzo<b>.closest()</b></code></a>
* <a href="#children"><code>bonzo<b>.children()</b></code></a>
* <a href="#width"><code>bonzo<b>.width()</b></code></a>
* <a href="#height"><code>bonzo<b>.height()</b></code></a>


<a name="parents"></a>
### parents()

`bonzo.parents()` TODO

<a name="closest"></a>
### closest()

`bonzo.closest()` TODO

<a name="children"></a>
### children()

`bonzo.children()` TODO

<a name="width"></a>
### width()

`bonzo.width()` TODO

<a name="height"></a>
### height()

`bonzo.height()` TODO

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
