<script>
export default {
 // props:["id", "title", "author", "releaseDate", "isLiked"],
 
 //Objetos que validen los props
  props: {
    id: {
      type:String,
      requerid:true,
    },
    title:{
      type:String,
      requerid:true,
    },
    author:{
      type:String,
      requerid:true,
    },
    releaseDate:{
      type:String,
      requerid:true,
    },
    isLiked:{
      type:String,
      requerid:false,
      default:"0",
      validator: function (value) {
        return value === "1" || value === "0";  
      },
    },
  },
 data() {
    return {
      detailsAreVisible: false,
      BookIsLiked: this.isLiked,
    };
 },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
    toggleFavorite(){
     if (this.BookIsLiked === "1") {
         this.BookIsLikedd = "0";
     }else{
        this.BookIsLiked = "1";
     }
    },
  },
};
</script>

<template>
  <li>
    <h2>{{ title }} {{ BookIsLiked === "1"  ? "(Liked)" : "(Not Liked)"}}</h2>

    <button type="button" @click="toggleDetails">
      {{ detailsAreVisible ? "Hide" : "Show" }}
    </button>

    <button type="button" @click="toggleFavorite">Toggle Favorite</button>

    <ul v-if="detailsAreVisible">
      <li><strong>Author:</strong>{{ author }}</li>
      <li><strong>Release Date:</strong>{{ releaseDate }}</li>
    </ul>
  </li>
</template>
