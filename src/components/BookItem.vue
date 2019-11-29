<template>
  <div>
    <h1>{{title}}</h1>
    <ul>
      <li>{{ book.title }}:{{book.author}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'BookItem',
  props: ['book']
  };
</script>

<style>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
}
</style>
