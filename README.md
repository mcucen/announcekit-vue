![](https://announcekit.app/images/logo@2x.png)

The easiest way to use AnnounceKit widgets in your VueJS App.

**Visit [https://announcekit.app](https://announcekit.app) to get started with AnnounceKit.**
[CodeSandbox Demo](https://codesandbox.io/s/announcekit-vue20-demo-jcfjf)

[Documentation](https://announcekit.app/docs/vuejs)

## Installation

```sh
yarn add announcekit-vue
```

## Usage

```js
<template>
    <nav>
      <ul>
        <li>
          <a href="/home">Home</a>
        </li>
        <li>
          <a href="/product">Product</a>
        </li>
        <li>
          <a href="#" class="ak-trigger">News
            <AnnounceKit
                catchClick=".ak-trigger"
                widget="https://announcekit.app/widgets/v2/31nbbO"
                :user="optional_UserData"
                :data='optional_SegmentationData' />
          </a>
        </li>
      </ul>
    </nav>
</template>

<script>
import AnnounceKit from "announcekit-vue";
export default {
  name: "App",
  components: {
    AnnounceKit
  }
};
</script>
```

## Props

Common props you may want to specify include:

- **`widget`** - The url of the widget. You can obtain it while creating or editing widget in AnnounceKit Dashboard.
- `style` - You can apply CSS rules to modify / tune the position of the widget.
- `catchClick` - Element selector to catch clicks and open the widget.
- `floatWidget` - Set true if the widget is a Float widget.
- `embedWidget` - Set true if the widget is a Embed widget.
- `user` - User properties (for user tracking)
- `data` - Segmentation data
- `onWidgetOpen` - Called when the widget is opened.
- `onWidgetClose` - Called when the widget is closed.
- `onWidgetResize` - Called when the widget is resized.
- `onWidgetUnread` - Called when unread post count of widget has been updated.
