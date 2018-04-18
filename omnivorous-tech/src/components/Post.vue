<template lang="pug">
  .post 
    .hello
      h1 {{ title }}
      .body(v-html="body")
    a(href="/") トップへ戻る
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'

Vue.use(VueAxios, axios)

const BLOG_ID = '819751833423889054';
const API_KEY = 'AIzaSyDSEiq6j_xAyNAAcz_1cyRzfIecHotCB6o';

export default {
  name: 'HelloWorld',
  props: ['id'],
  data(){
    return {
      title: 'Blog title',
      body: 'Body'
    }
  },
  mounted(){
    var api = "https://www.googleapis.com/blogger/v3/blogs/"+BLOG_ID+"/posts/"+this.id;
    Vue.axios.get(api,{params:{key: API_KEY}}).then((response) => {
      this.title = response.data.title;
      this.body = response.data.content;
    })
  },
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
