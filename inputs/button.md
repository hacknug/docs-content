---
title: Button
description: A native HTML button element.
---

<InputPageHero
title="Button input"
icon="IconInputButton"
:pro="false"
project-price=""
data-price=""></InputPageHero>

The `button` input uses HTML's [native button element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button). The `label` prop is used to populate the text of the button — or alternatively you can use the default slot.

<example
name="Button input"
file="/_content/examples/button/button.vue"></example>

## Props & Attributes

The `button` input is unique in that it does not actively receive input other than a transient click. However, nearly all of the base input props still technically exist on the input.

Importantly the `ignore` prop is automatically set to `true` — meaning even if a button is given a value, it will not communicate it with the parent form. However, this default behavior can be changed by setting the prop `:ignore="false"`.

<reference-table input="button">
</reference-table>

## Section keys

You can target a specific section of an input using that section's "key". Read more about sections [here](/essentials/inputs#sections).

<div>
  <formkit-input-diagram
    class="input-diagram--button"
    :schema="[
      {
        name: 'outer',
        children: [
          {
            name: 'messages',
            position: 'right',
            children: [
              {
                name: 'message',
                content: 'Validation messages about the button.',
                position: 'right'
              }
            ]
          },
          {
            name: 'wrapper',
            position: 'right',
            children: [
              {
                name: 'input',
                position: 'left',
                class: 'flex button button--pro',
                children: [
                  {
                    name: 'prefix',
                    content: '🤟'
                  },
                  {
                    name: 'label',
                    content: 'Submit application',
                  },
                  {
                    name: 'suffix',
                    position: 'right',
                    content: '🚀'
                  }
                ]
              },
            ]
          },
          {
            name: 'help',
            content: 'Click this button to submit your application. '
          }
        ]
      }
    ]"
  >
  </formkit-input-diagram>
</div>

<reference-table type="sectionKeys" primary="section-key" :without="['inner']">
</reference-table>
