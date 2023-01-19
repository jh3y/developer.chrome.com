---
layout: 'layouts/doc-post.njk'
title: The CSS Anchor Positioning API
description: The CSS Anchor Positioning API provides a way to tether elements to one another whilst optionally being mindful of container bounds.
subhead: The CSS Anchor Positioning API provides a way to tether elements to one another whilst optionally being mindful of container bounds.
authors:
  - jheyy
date: 2023-01-19
---

The CSS Anchor Positioning API provides developers with a way to tether elements to one another without the need for particular markup structures. The API makes it possible for developers to use the position of one element as the values used when positioning another. Optionally, developers can use a fallback mechanism where the API will attempt to keep the anchored element within the bounds of its container.

## Current status

* The CSS Anchor Positioning API is planned for launch in Chrome <TBD>, available in stable in <TBD> (check the [Chrome Roadmap](https://chromestatus.com/roadmap) for updates).
* There is a polyfill available at [https://github.com/oddbird/css-anchor-positioning](https://github.com/oddbird/css-anchor-positioning).

## Concepts and usage (Explain the problem here and give example usage explaining the properties and fallback mechanism)


## HTML attributes
<!-- Check on the anchor attribute usage -->

[`anchor`](/docs/web-platform/popover-api/popover-attribute)

## CSS features

[`anchor-name`](/docs/web-platform/popover-api/backdrop-pseudo-element)

[`position-fallback`](/docs/web-platform/popover-api/backdrop-pseudo-element)

[`@position-fallback`](/docs/web-platform/popover-api/open-pseudo-class)

[`anchor()`](/docs/web-platform/popover-api/open-pseudo-class)

[`anchor-size()`](/docs/web-platform/popover-api/open-pseudo-class)


## Interfaces

### Extensions to `HTMLElement`

Properties:

[`anchor`](/docs/web-platform/popover-api/popover-property):

`onfallback` event?:

Events:

[`fallback`](/docs/web-platform/popover-api/beforetoggle-event)

## Examples

{% Aside %}
This section shows basic usage of the API; for more substantial code including numerous complete examples, check out [CSS Anchoring: Tether elements without worrying about keeping them in view](/blog/pop-ups-theyre-making-a-resurgence/) by Jhey Tompkins.
{% endAside %}

<!-- How to anchor -->

```css
.anchor {
  anchor-name: --anchor;
}

.anchored {
  top: anchor(--anchor bottom);
}
```

<!-- Show position-fallback usage -->


<!-- Will we have some form of position-fallback detection event? -->

```js
  anchored.addEventListener('fallback', (event) => {
    // Anchored thing has moved
  })
```

## Feedback

Your feedback on the API is welcome. Open an issue on the [CSSWG Drafts repository](https://github.com/w3c/csswg-drafts/labels/css-anchor-1) to get involved. 

## See also

* [CSS Anchoring: Tether elements without worrying about keeping them in view](/blog/pop-ups-theyre-making-a-resurgence/), by Jhey Tompkins
* [CSS Anchor Positioning spec](https://drafts.csswg.org/css-anchor-1/)