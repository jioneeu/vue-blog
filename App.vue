<template>
  <div id="app">
    <blog-header />
    <div>
      <router-view />
    </div>
    <blog-footer />
  </div>
</template>

<script>
import BlogHeader from "./views/components/Header";
import BlogFooter from "./views/components/Footer";

export default {
  components: { BlogHeader, BlogFooter },
};
</script>

<style lang="scss">
html {
  background-color: #f5f5f5;
  color: rgba(0, 0, 0, 0.8);
}

@media only screen and (min-width: 1025px) {
  body {
    margin: 0;
  }

  ::selection {
    background: rgba(225, 225, 243, 0.2);
    text-shadow: none;
  }
}

@media only screen and (min-width: 320px) and (max-width: 480px) {
  body {
    margin: 0 1.2em;
    padding: 0 5px;

    .sections {
      font-size: 13px;

      h3 {
        font-size: 14px;
      }

      p.description {
      // これ嫌だな
        width: 100% !important;
      }
    }
  }
}
</style>