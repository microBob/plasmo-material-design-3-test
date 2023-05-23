<template>
  <div id="goji-card-host">Hello World from the Goji Card</div>
</template>

<script lang="ts">
import css from "data-text:~/contents/card.css"
import type { PlasmoGetStyle } from "plasmo"

/**
 * Returns a newly created style element with the css content set as its text content
 *
 * @return {PlasmoGetStyle} A newly created style element
 */
const getStyle: PlasmoGetStyle = (): HTMLStyleElement => {
  const style = document.createElement("style")
  style.textContent = css
  return style
}

export default {
  plasmo: {
    getStyle
  },
  setup() {},
  mounted() {}
}
</script>
