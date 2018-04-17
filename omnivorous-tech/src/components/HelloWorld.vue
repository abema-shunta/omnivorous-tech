<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="https://twitter.com"
          target="_blank"
        >
          Twitter
        </a>
      </li>
      <li>
        <a
          href="https://facebook.com"
          target="_blank"
        >
          Facebook
        </a>
      </li>
      <li>
        <a
          href="https://forum.vuejs.org"
          target="_blank"
        >
          Github
        </a>
      </li>
      <br>
    </ul>
    <h2>Recent Articles</h2>
    <ul>
      <li>Comming Soon...</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Omnivorous Tech'
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
