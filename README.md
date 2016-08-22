# weex-hello

This is a example extension for weex-html5, which is a self defined component to display a 'hello xxx' infomation panel in the weex page.

## specs

This is a definition of this `weex-hello` component. It suggests what attributes the components should take, what special style names it support, and what events it can listen to.

### attr

* `value`: the displaying content after 'Hello'.

### style

* `txt-color`: the color of the displaying message.
* `bg-color`: the background color of the displaying message.

### event

* `click`: will parse the current 'value' to the event object in the event handler.

## how to use

Just place the tag `<weex-hello>` no matter where you like to display the info. For example, You want to play a msg 'hello WEEX', and when click on it, you want to display a alert message to show the component's value attribute. Then you can use the `weex-hello` component to do it.

```html
<template>
  <div>
    <weex-hello style="txt-color:#fff;bg-color:green" value="WEEX" onclick="handleClick"></weex-hello>
  </div>
</template>

<script>
  module.exports = {
    methods: {
      handleClick (e) {
        alert('e.value : ' + e.value)
      }
    }
  }
</script>
```

## where to publish

We suggest you publish the component on npm, with the name of `weex-xxx`. For this project, we published the `weex-hello` component to npm, so anyone can just require and use it.

## help

### what is Weex ?

Weex is a project for developers to write code once with web technologies and run it everywhere. [site](http://alibaba.github.io/weex/)

### how to extend Weex with self defined components and APIs ?

weex-hello is a example for extending components. The document for extending weex components and APIs is here: [extend to web](http://alibaba.github.io/weex/doc/advanced/extend-to-html5.html)
