<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <ListItem v-bind:item-data="CLIPlugins"></ListItem>
    <ListItem v-bind:item-data="essentialLinks"></ListItem>
    <ListItem v-bind:item-data="ecosystem"></ListItem>
  </div>
</template>

<script>
import ListItem from './ListItem.vue';
export default {
  name: 'HelloWorld',
  components: {
    ListItem
  },
  data: function() {
    return {
      CLIPlugins: {
        title: 'Installed CLI Plugins',
        buttons: [
        {url: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel', text: 'babel'},
        {url: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint', text: 'eslint'}
        ]
      },
      essentialLinks: {
        title: 'Essential Links',
        buttons: [
        {url: 'https://vuejs.org', text: 'Core Docs'},
        {url: 'https://forum.vuejs.org', text: 'Forum'}, 
        {url: 'https://chat.vuejs.org', text: 'Community Chat'},
        {url: 'https://twitter.com/vuejs', text: 'Twitter'},
        {url: 'https://news.vuejs.org', text: 'News'},

        ]
      },
      ecosystem: {
        title: 'Ecosystem',
        buttons: [
        {url: 'https://router.vuejs.org', text: 'vue-router'},
        {url: 'https://vuex.vuejs.org', text: 'vuex'},
        {url: 'https://github.com/vuejs/vue-devtools#vue-devtools', text: 'vue-devtools'},
        {url: 'https://vue-loader.vuejs.org', text: 'vue-loader'},
        {url: 'https://github.com/vuejs/awesome-vue', text: 'awesome-vue'},
        ]
      }
    };
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 
</style>
