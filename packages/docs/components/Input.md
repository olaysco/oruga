---
title: Input
---

# Input

> Get user Input. Use with Field to access all functionalities

---

## Examples

### Base

::: demo

```html
<template>
  <section>
    <o-field label="Name">
      <o-input v-model="name"></o-input>
    </o-field>

    <o-field label="Email" variant="danger" message="This email is invalid">
      <o-input type="email" value="john@" maxlength="30"> </o-input>
    </o-field>

    <o-field
      label="Username"
      variant="success"
      message="This username is available"
    >
      <o-input value="johnsilver" maxlength="30"></o-input>
    </o-field>

    <o-field label="Password">
      <o-input type="password" value="iwantmytreasure" password-reveal>
      </o-input>
    </o-field>

    <o-field label="Message">
      <o-input maxlength="200" type="textarea"></o-input>
    </o-field>

    <o-field>
      <o-input placeholder="No label"></o-input>
    </o-field>

    <o-field label="Rounded">
      <o-input placeholder="No label" rounded></o-input>
    </o-field>

    <o-field label="Success" variant="success">
      <o-input placeholder="Success"></o-input>
    </o-field>

    <o-field
      label="Error"
      variant="danger"
      message="You can have a message too"
    >
      <o-input placeholder="Error"></o-input>
    </o-field>

    <o-field label="Info" variant="info">
      <o-input placeholder="Info"></o-input>
    </o-field>

    <o-field label="Warning" variant="warning">
      <o-input placeholder="Warning"></o-input>
    </o-field>

    <o-field label="Disabled">
      <o-input placeholder="Disabled" disabled></o-input>
    </o-field>

    <o-field>
      <o-input placeholder="Large" size="large" icon="user"> </o-input>
    </o-field>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        name: "John Silver"
      };
    }
  };
</script>
```

:::

### Base

::: demo

```html
<template>
  <section>
    <h3 class="subtitle">With Material Design Icons</h3>
    <o-field>
      <o-input
        placeholder="Search..."
        type="search"
        icon="search"
        icon-clickable
        @icon-click="searchIconClick"
      >
      </o-input>
    </o-field>

    <o-field>
      <o-input
        placeholder="Email"
        v-model="email"
        type="email"
        icon="envelope"
        icon-right="times-circle"
        icon-right-clickable
        @icon-right-click="clearIconClick"
      >
      </o-input>
    </o-field>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        email: ""
      };
    },
    methods: {
      searchIconClick() {
        alert("You wanna make a search?");
      },
      clearIconClick() {
        this.email = "";
        alert("Email cleared!");
      }
    }
  };
</script>
```

:::

## Props

| Prop name             | Description                                                 | Type           | Values                                  | Default                    |
| --------------------- | ----------------------------------------------------------- | -------------- | --------------------------------------- | -------------------------- |
| size                  | Vertical size of input, optional                            | string         | `small`, `medium`, `large`              |                            |
| expanded              | Makes input full width when inside a grouped or addon field | boolean        | -                                       |                            |
| loading               | Adds the loading state to the input                         | boolean        | -                                       |                            |
| rounded               | Makes the element rounded                                   | boolean        | -                                       |                            |
| icon                  | Icon name to be added                                       | string         | -                                       |                            |
| iconPack              | Icon pack to use                                            | string         | `mdi`, `fa`, `fas`, `far`, `fad`, `fal` |                            |
| autocomplete          | Native options to use in HTML5 validation                   | string         | -                                       |                            |
| maxlength             | Same as native maxlength, plus character counter            | number\|string | -                                       |                            |
| useHtml5Validation    | Enable html 5 native validation                             | boolean        | -                                       | "useHtml5Validation": true |
| statusIcon            | Show status icon using field and variant prop               | boolean        | -                                       | "statusIcon": true         |
| validationMessage     | The message which is shown when a validation error occurs   | string         | -                                       |                            |
| v-model               |                                                             | number\|string | -                                       |                            |
| type                  | Input type, like native                                     | string         | `Any native input type`, `and textarea` | 'text'                     |
| passwordReveal        | Adds the reveal password functionality                      | boolean        | -                                       |                            |
| iconClickable         | Makes the icon clickable                                    | boolean        | -                                       |                            |
| hasCounter            | Show character counter when maxlength prop is passed        | boolean        | -                                       | 'input.counter': false     |
| iconRight             | Icon name to be added on the right side                     | string         | -                                       |                            |
| iconRightClickable    | Make the icon right clickable                               | boolean        | -                                       |                            |
| rootClass             |                                                             | string         | -                                       |                            |
| controlExpandedClass  |                                                             | string         | -                                       |                            |
| controlIconLeftClass  |                                                             | string         | -                                       |                            |
| controlIconRightClass |                                                             | string         | -                                       |                            |
| inputClass            |                                                             | string         | -                                       |                            |
| roundedClass          |                                                             | string         | -                                       |                            |
| iconLeftClass         |                                                             | string         | -                                       |                            |
| iconRightClass        |                                                             | string         | -                                       |                            |
| counterClass          |                                                             | string         | -                                       |                            |
| counterInvisibleClass |                                                             | string         | -                                       |                            |
| sizeClass             |                                                             | string         | -                                       |                            |
| variantClass          |                                                             | string         | -                                       |                            |

## Events

| Event name | Type      | Description |
| ---------- | --------- | ----------- |
| blur       | undefined |
| focus      | undefined |
| input      | undefined |

## Style

| CSS Variable                        | SASS Variable                 | Default                               |
| ----------------------------------- | ----------------------------- | ------------------------------------- |
| --oruga-input-background-color      | \$input-background-color      | #ffffff                               |
| --oruga-input-border-color          | \$input-border-color          | \$grey-lighter                        |
| --oruga-input-border-radius         | \$input-border-radius         | \$base-border-radius                  |
| --oruga-input-rounded-border-radius | \$input-rounded-border-radius | \$base-rounded-border-radius          |
| --oruga-input-border                | \$input-border                | 1px solid transparent                 |
| --oruga-input-box-shadow            | \$input-box-shadow            | inset 0 1px 2px hsla(0,0%,4%,.1)      |
| --oruga-input-color                 | \$input-color                 | #363636                               |
| --oruga-input-control-icon-zindex   | \$input-control-icon-zindex   | 4                                     |
| --oruga-input-control-icon-color    | \$input-control-icon-color    | \$grey-lighter                        |
| --oruga-input-counter-font-size     | \$input-counter-font-size     | .75rem                                |
| --oruga-input-counter-margin        | \$input-counter-margin        | .25rem 0 0 .5rem                      |
| --oruga-input-height                | \$input-height                | \$control-height                      |
| --oruga-input-line-height           | \$input-line-height           | \$base-line-height                    |
| --oruga-input-margin                | \$input-margin                | 0                                     |
| --oruga-input-max-width             | \$input-max-width             | 100%                                  |
| --oruga-input-padding               | \$input-padding               | calc(.375em - 1px) calc(.625em - 1px) |
| --oruga-input-textarea-max-height   | \$input-textarea-max-height   | 600px                                 |
| --oruga-input-textarea-min-height   | \$input-textarea-min-height   | 120px                                 |
| --oruga-input-textarea-padding      | \$input-textarea-padding      | 0.625em                               |
| --oruga-input-width                 | \$input-width                 | 100%                                  |
