<script>
export default {
  data() {
    return {
      books: [
        {
          id: 1,
          title: "Narnia",
          author: "C.S Lewis",
          releaseDate: "1999-12-01",
        },
        {
          id: 2,
          title: "Narnia II",
          author: "C.S Lewis",
          releaseDate: "1999-12-01",
        },
        {
          id: 3,
          title: "Narnia III",
          author: "C.S Lewis",
          releaseDate: "1999-12-01",
        },
      ],
    };
  },
};
</script>

<template>
  <h1>My books</h1>
  <ul>
    <book-info  
        id-1
        title="Narnia I"
        author="C.S Lewis"
        release-date="1769-12-01"
        is-liked="1"></book-info>
    <book-info 
        id="1"
        title="Narnia II"
        author="C.S Lewis"
        release-date="1889-12-01"
        is-liked="0"></book-info>
    <book-info 
        id="1"
        title="Narnia III"
        author="C.S Lewis"
        release-date="1799-12-01"
        is-liked="1"></book-info>
  </ul>
</template>

<style>
h1 {
  color: blueviolet;
}

</style>
