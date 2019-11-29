<template>
  <form v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)" class="" action="#" method="post">
      <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title">
      <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author">
      <button type="submit" name="button">Add Book</button>
      </form>

  </form>
</template>

<script>
export default {
  name: 'BookForm',
  props: ['books'],
  data() {
      return {
        bookTitle: '',
        bookAuthor: ''
      }
  },
  methods:{
    bookSubmit(bookTitle, bookAuthor){
      this.$emit('addbook', bookTitle, bookAuthor)
}
  }
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
