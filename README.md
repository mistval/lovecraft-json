# Lovecraft JSON

H.P. Lovecraft works formatted as JSON. Experience the great classics like you never have before... as a machine!

## Format

The format is basically like this:

```js
{
  "title": "Story title",
  "published": "1920",
  "order": 0, // This is always 0, for now.
  "image": "", // This is always empty, for now.
  "description": "A story about monsters and zombies.",
  "body": [
    {
      "type": "center",
      "children": [
        {
          "type": "paragraph",
          "text": "Some centered text"
        }
      ]
    },
    {
      "type": "right",
      "children": [
        {
          "type": "paragraph",
          "text": "Some right aligned text"
        }
      ]
    },
    {
      "type": "breakline"
    },
    {
      "type": "paragraph",
      "text": "<i>One paragraph of text</i>"
    },
    {
      "type": "paragraph",
      "text": "<b>Another paragraph of text</b>"
    },
    {
      "type": "blockquote",
      "children": [
        {
          "type": "paragraph",
          "text": "“Some text in a blockquote.”"
        }
      ]
    },
    {
      "type": "horizontal-rule"
    }
  ]
}
```

All story text is inside of `paragraph` elements, potentially nested as children of `center`, `right`, or `blockquote` elements.

The text property of `paragraph` elements can contain some basic HTML tags, including `<i>` and `<b>` (I think that's all).

`blockquote` can potentially contain `center` elements as children.

You should always add one line break between elements. `breakline` suggests that you should add an extra one.

`horizontal-rule` is equivalent to an HTML `<hr>`. There's only one so far in the whole library (in The Mysterious Ship).

The story text comes from [The H.P. Lovecraft Archive](http://www.hplovecraft.com/). Most of the descriptions are adapted from Wikipedia synopses, some are just the first sentence of the story, others are written by YT.

## TODO

* Add poetry and other works
* Add The Thing in the Moonlight
