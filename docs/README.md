📢 Don't fork this project. Use, [contribute](https://github.com/vtex-apps/awesome-io#contributing), or open issues through [Store Discussion](https://github.com/vtex-apps/store-discussion).
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-0-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

# Product Quantity

The Product Quantity allows users to a **add a chosen amount** of the displayed product in their cart.

![product-quantity](https://user-images.githubusercontent.com/52087100/70237475-0f4bd900-1746-11ea-9af2-38f794f4a3dd.png)

## Configuration 

1. Import the Product Quantity to your dependencies on `manifest.json` file.

```json
  "dependencies": {
    "vtex.product-quantity": "1.x"
  }
```

2. Add the Product Quantity block to your theme. If you want to display it on a Product Page, you should declare the `product-quantity` in the `store.product` block. In order to display it in a Product Summary block, i.e. in blocks that use Product Summary, declare the `product-summary-quantity` in the `product-summary.shelf` block.

Check an example of a Product Details Page built using Flex Layout with the `product-quantity` below:

```json
  "flex-layout.col#product-price": {
    "props": {
      "preventVerticalStretch": true,
      "rowGap": 0
    },
    "children": [
      "product-name",
      "product-price#product-details",
      "product-separator",
+      "product-quantity",
      "sku-selector",
      "flex-layout.row#buy-button",
      "availability-subscriber",
      "shipping-simulator",
      "share"
    ]
  },
  "product-quantity": {
    "props": {
      "warningQuantityThreshold": 9999999
    }
  },
```

| Prop name | Type | Description | Default Value |
| --- | --- | --- | --- |
| `warningQuantityThreshold` | `Number` | Displays the quantity of remaining items in stock if the available quantity is less than or equal to the value given to this property. Default: 0 (does not appear). | `0` |
| `size` | `NumericSize`| Preset values `font-size` and `padding` to the component | `'small'` |
| `showLabel` | `boolean` | If it should show a label | `true` |

### NumericSize

You can check how big these values are and what classes it aplies by going to the [styleguide docs](https://styleguide.vtex.com/#/Components/Forms/NumericStepper).

| Value | Description |
| --- | --- |
| `'small'` | Small size |
| `'regular'` | Medium size |
| `'large'` | Large size |


## Customization

In order to apply CSS customizations in this and other blocks, follow the instructions given in the recipe on [Using CSS Handles for store customization](https://vtex.io/docs/recipes/style/using-css-handles-for-store-customization). 

| CSS Handles                  |
| ---------------------------- | 
| `quantitySelectorContainer`  |
| `availableQuantityContainer` | 
| `quantitySelectorTitle`      |
| `quantitySelectorStepper`    |
| `summaryContainer`           | 

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!