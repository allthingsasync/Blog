---
title: Markdown inside shortcodes
---

Some shortcodes, like `card` or `alert`, support
markdown content inside them.

## Components that support markdown

- [Card](/docs/shortcode-card)
- [Fullbleed](/docs/shortcode-fullbleed)
- [Aside](/docs/shortcode-aside)

## Be careful with indentation

You may want to indent content inside a shortcode for
more readability, but be careful - indentation in 4 spaces is
considered as a `pre` block in markdown. For example, this code:

{% raw %}
```
{% fullbleed "yellow-soft", false %}

    ## Test data

    - item 1
    - item 2
    - item 3

    This is a text
    And this is text, too. Another text is ok
{% endfullbleed %}
```
{% endraw %}

Will be rendered like this:

{% fullbleed "yellow-soft", false %}

    ## Test data

    - item 1
    - item 2
    - item 3

    This is a text
    And this is text, too. Another text is ok
{% endfullbleed %}

While this code:

{% raw %}
```
{% fullbleed "yellow-soft", false %}

## Test data

- item 1
- item 2
- item 3

This is a text
And this is text, too. Another text is ok
{% endfullbleed %}
```
{% endraw %}

Works as expected:

{% fullbleed "yellow-soft", false %}

## Test data

- item 1
- item 2
- item 3

This is a text
And this is text, too. Another text is ok
{% endfullbleed %}
