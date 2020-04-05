# Tips and tricks for working with gotoB.js

This is intended to be a tutorial for [gotob.js](https://github.com/fpereiro/gotoB), currently covering the 1.2.x series.

## Pronounciation.

gotoB, despite it's spelling, is pronounced "gah-tov". There is a russian pun to thank for that. ( [source](https://youtube.com/watch?v=t12fLfyc2T0), at 26:33 )

## Getting started

Before you start using gotoB, I recommend at least learning [dale](https://github.com/fpereiro/dale) and [lith](https://github.com/fpereiro/lith). It's not hard and it won't take long, but it's very helpful for understanding examples. Also, I don't recommend trying to do what I did, and construct a bundle from the various ustack repos. Using the .min.js file is by far the easiest way to get started, as it incorporates the correct versions of some of it's depdencies. Also, reading the basic tutorial on the gotoB.js readme will help 

## Reading the Source

If you do decide to read the gotoB source, you will also want to learn the basics of [teishi](https://github.com/fpereiro/teishi) and [recalc](https://github.com/fpereiro/recalc), as there feature 

## Some edge cases

One of the more natural uses of gotoB is to render a list or a table of information. One thing you can do is nest calls to `B.view`, so that you only redraw only the relevant subviews. If you make a table row, or a table cell into a subview, be sure to add `tag: 'tr'` or `tag: 'td'` to the same object argument that specifies the events that the view listens to.

Quick example:

```js
var b = B.view(['State', 'var'], {tag: 'td'}, function(x) {
    // return contents of td here
});
```
