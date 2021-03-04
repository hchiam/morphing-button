# `morphing_button` [![version](https://img.shields.io/github/release/hchiam/morphing_button)](https://github.com/hchiam/morphing_button/releases)

[Live demo](https://codepen.io/hchiam/pen/BaQNXom)

[<img src="demo.gif" height="300">](https://codepen.io/hchiam/pen/BaQNXom)

```js
https://cdn.jsdelivr.net/gh/hchiam/morphing_button@main/morphing_button.js
```

```js
https://cdn.jsdelivr.net/gh/hchiam/morphing_button@1.1.0/morphing_button.js
```

## Example usage:

### Just include and add classes:

```html
<button id="test" class="morphing_button fill-screen">test</button>
<script
  src="https://cdn.jsdelivr.net/gh/hchiam/morphing_button@2.0.0/morphing_button.js"
  integrity="sha384-4k/kXfx1xGoYDvvWWRlSepBJbkbLbSCpXugIbxGNEP4S7SUmIiDO6ZkAsBFNmrO0"
  crossorigin="anonymous"
></script>
```

### Or for more fine-grained control, omit `.morphing_button`:

- `Morphing_button.setup(button)`
- `Morphing_button.morph(button)`
- `Morphing_button.revert(button)`

```html
<!-- without the .morphing_button class: -->
<button id="test" class="fill-screen">test</button>
<script
  src="https://cdn.jsdelivr.net/gh/hchiam/morphing_button@2.0.0/morphing_button.js"
  integrity="sha384-8KxKsoiL1qGLyP/NoWrQjjdXp3VO98CGGDpLYgNzaAKswhhUDrad981WsRkYluRA"
  crossorigin="anonymous"
></script>
<script>
  var btn = document.querySelector("#test");
  Morphing_button.setup(btn);
  btn.addEventListener("click", function () {
    Morphing_button.morph(btn);
    setTimeout(function () {
      Morphing_button.revert(btn);
    }, 2000);
  });
</script>
```

## For development:

```bash
# to get the thing to put into integrity="...":
bash get-integrity.sh
```
