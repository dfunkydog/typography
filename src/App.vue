<template>
  <div id="app">
    <button v-on:click="basic = !basic" type="button">Hide text</button>
    <HelloWorld/>
    <BasicText v-if="basic"></BasicText>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import BasicText from './components/BasicText'

export default {
  name: 'App',
  components: {
    HelloWorld,
    BasicText
  },
  data () {
    return {
      basic: true,
      forms: false
    }
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
    @include nls-html(21);
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
