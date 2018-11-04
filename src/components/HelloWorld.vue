<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{from}}</h1>
    <h1>{{job}}</h1>
    <h1>{{time}}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="https://vuejs.org"
          target="_blank"
        >
          Core Docs
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Forum
        </a>
      </li>
      <li>
        <a
          href="https://chat.vuejs.org"
          target="_blank"
        >
          Community Chat
        </a>
      </li>
      <li>
        <a
          href="https://twitter.com/vuejs"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <br>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li>
        <a
          href="http://router.vuejs.org/"
          target="_blank"
        >
          vue-router
        </a>
      </li>
      <li>
        <a
          href="http://vuex.vuejs.org/"
          target="_blank"
        >
          vuex
        </a>
      </li>
      <li>
        <a
          href="http://vue-loader.vuejs.org/"
          target="_blank"
        >
          vue-loader
        </a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/awesome-vue"
          target="_blank"
        >
          awesome-vue
        </a>
      </li>
    </ul>
  </div>
</template>
<template>
  <div>
    <div class="field is-grouped is-grouped-multiline">
      <p class="control">
        <button type="button" class="button" @click="add" :disabled="images.length===10">Add</button>
      </p>
      <p class="control">
        <button type="button" class="button" @click="remove" :disabled="images.length===0">Remove</button>
      </p>
      <p class="control">
        <button type="button" class="button" @click="show">Show</button>
      </p>
    </div>
    <p>
      To show the viewer, you can click these images too.
    </p>
    <div v-viewer="options" class="images clearfix">
      <template v-for="{source, thumbnail} in images">
        <img :src="thumbnail" :data-source="source" class="image" :key="source" :alt="source.split('?image=').pop()">
      </template>
    </div>
  </div>
</template>
<script>

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      from: 'hangzhou',
      job:'前端',
      time:'10-24'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
