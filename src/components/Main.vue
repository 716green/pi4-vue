<template>
  <div class="main">
    <h1>A better VueJS boilerplate</h1>
    <p>
      A better boilerplate from <a href="https://www.github.com/71green">716green</a>
    </p>
    <h3>{{this.sectionTitle}}</h3>
    <!-- <h4>{{this.items}}</h4> -->
    <ul>
      <li v-for="item in this.items" :key="item">{{item}}</li>
    </ul>
    {{this.sample}}
    
  </div>
</template>

<script>
export default {
  name: 'Main',
  props: {
    sectionTitle: {
      type: String,
      default: ""
    },
  },
  data() {
    return {
      sample: "This is a sample string",
      items: {
        a: 'value1',
        b: 'value2',
        c: 'value3'
        }
    }
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
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
