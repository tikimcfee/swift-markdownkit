# Sample document
## A few lines of Markdown text

**(make-drawing)**

Returns a new, empty drawing. A _drawing_ consists of a sequence of drawing instructions and
drawing state consisting of the following components:

   - Stroke color (set via `set-color`)
   - Fill color (set via `fill-color`)
   - Shadow (set via `set-shadow` and `remove-shadow`)
   - Transformation (add transformation via `enable-transformation` and remove via `disable-transformation`)

**(enum-set-indexer _enum-set_)**

Returns a unary procedure that, given a symbol that is in the universe of _enum-set_,
returns its 0-origin index within the canonical ordering of the symbols in the universe;
given a value not in the universe, the unary procedure returns `#f`.

Returns a unary procedure that, given a symbol that is in the universe of _enum-set_,
returns its 0-origin index within the canonical ordering of the symbols

```
(let* ((e (make-enumeration '(red green blue)))
(i (enum-set-indexer e)))
(list (i 'red) (i 'green) (i 'blue) (i 'yellow)))
⇒ (0 1 2 #f)
```

The `enum-set-indexer` procedure could be defined as follows using the `memq` procedure.

> And this is a fancy
> blockquote `code block`.