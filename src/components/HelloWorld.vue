<template>
<div class="hello"> </div>
<ul id="example-1">
<li v-show='toggle' v-for="item in items" :key="item.message">
{{ item.message }}
</li>
</ul>

<div id="example-2">
<button @click='toggle = !toggle'>Afficher / Masquer</button>
</div>

</template>

<script>
export default {
name: 'HelloWorld',
props: {
msg: String
},
data () {

return {
toggle: true,
items: [
{ message: 'michmich' },
{ message: 'balou' },
{ message: 'rené' },
{ message: 'zincou' },
{ message: 'alex' }
],
}
},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
