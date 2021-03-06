---
$category@: ads-analytics
formats:
  - websites
teaser:
  text: Provides a way to display and stick ad content at the bottom of the page.
---

<!---
Copyright 2016 The AMP HTML Authors. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS-IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

# amp-sticky-ad

## Behavior

- There can be only one `<amp-sticky-ad>` in an AMP document. The `<amp-sticky-ad>` should only have one direct child: `<amp-ad>`. **Note**: Make sure you include any required scripts for the `<amp-ad>` component.
- The sticky ad appears at the bottom of a page.
- The sticky ad introduces a full-width blank container and then fills the sticky ad based on the width and height of the `<amp-ad>`.
- The height of the sticky-ad is whatever its child needs up to its max-height.
- The max-height of the sticky-ad is 100px, if the height exceeds 100px then the height would be 100px and overflow content will be hidden.
- The width of the sticky-ad is set to 100% using CSS and cannot be overridden.
- The opacity of the sticky-ad is set to 1 using CSS and cannot be overridden.
- The background color of the sticky-ad can be customized to match the page style. However, any semi-transparent or transparent background will not be allowed and will be changed to a non-transparent color.
- When scrolled to the bottom of the page, the viewport is automatically padded with the additional height of the sticky ad, so that no content is ever hidden.
- When in landscape mode, the sticky ad is center-aligned.
- The sticky ad can be dismissed and removed by a close button.
- If no ad is filled, the sticky ad container will collapse and will no longer be visible.

Example:

```html
<amp-sticky-ad layout="nodisplay">
  <amp-ad
    width="320"
    height="50"
    type="doubleclick"
    data-slot="/35096353/amptesting/formats/sticky"
  >
  </amp-ad>
</amp-sticky-ad>
```

## Attributes

<table>
  <tr>
    <td width="40%"><strong>layout (required)</strong></td>
    <td>Must be set to <code>nodisplay</code>.</td>
  </tr>
</table>

## Styling

The `amp-sticky-ad` component can be styled with standard CSS.

- The sticky ad container style can be set through the `amp-sticky-ad` CSS class.
- The close button style can be set through the `amp-sticky-ad-close-button` CSS class.
- The padding bar between the ad and the close button style can be set through the `amp-sticky-ad-top-padding` CSS class.

## Validation

See [amp-sticky-ad rules](https://github.com/ampproject/amphtml/blob/master/extensions/amp-sticky-ad/validator-amp-sticky-ad.protoascii) in the AMP validator specification.
