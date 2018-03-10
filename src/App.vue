<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <TextContent/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TextContent from './components/TextContent'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TextContent
  }
}
</script>

<style lang="scss">
  @font-face {
    font-family: 'sourcesans';
    src: url('./assets/SourceSansVariable-Roman.ttf') format('truetype-variations'), url('./assets/SourceSansVariable-Roman.ttf') format('truetype');
  }
  @import './scss/index.scss';
  html {
    @include nls-html(16);
  }
  body{
    @include nls-body("rem");
    font-family: sourcesans;
    margin: 0;
  }
  h1 {
    @include nls-heading(3, "rem");
  }
  h2 {
    @include nls-heading(2, "rem");
  }
  h3 {
    @include nls-heading(1, "rem");
  }
  h4 {
    @include nls-heading(0, "rem");
    font-weight: 400;
  }
  p, ul, ol, pre, table, blockquote {
    @include nls-margins();
  }

</style>
