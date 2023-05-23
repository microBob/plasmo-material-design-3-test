<template>
  <div id="goji-card-host">
    <p>Hello World from the Goji Card</p>
    <md-outlined-button>md-outlined-button</md-outlined-button>
  </div>
</template>

<script lang="ts">
import { MdOutlinedButton } from "@material/web/button/outlined-button.js"
import css from "data-text:~/contents/card.css"
import type { PlasmoCSConfig, PlasmoGetStyle } from "plasmo"

export const config: PlasmoCSConfig = {
  matches: ["https://www.google.com/*"],
  all_frames: true
}

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
