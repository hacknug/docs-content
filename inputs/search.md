---
title: Search
description: A native HTML search input.
---

<InputPageHero
title="Search input"
icon="IconInputSearch"
:pro="false"
project-price=""
data-price=""></InputPageHero>

The `search` input uses HTML's [native search input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search). Generally, search inputs are the same as text inputs, but may have different styling or features based on the browser. For example, browsers often add a small "X" to clear the input when it has a value.

<example
name="Search input"
file="/_content/examples/search/search.vue"></example>

## Props & Attributes

The `search` input has no unique props but can make use of the following universal
FormKit props.

<reference-table input="search" :attrs="['maxlength', 'minlength', 'placeholder']">
</reference-table>

## Section keys
You can target a specific section of an input using that section's "key". Read more about sections [here](/essentials/inputs#sections).

<div>
  <formkit-input-diagram
    prefix-content="🔍"
    suffix-content="→"
    label-content="Search everything"
    input-content="Best climate for tomatoes"
    help-content="Enter search term and press enter to search."
    message-content="Please enter a search term."
  >
  </formkit-input-diagram>
</div>

<reference-table type="sectionKeys" primary="section-key">
</reference-table>
