<script setup>
import { bookData } from "../data/data.js";
import Book from "../components/Book.vue";

const handleBookClick = (id) => {
  console.log(`This is Book ${id}`);
};
</script>

<template>
  <div class="flex flex-col items-center mt-4">
    <h1 class="text-white text-5xl font-extrabold my-5">Best Selling Books</h1>
    <div class="flex flex-col gap-8">
      <div :key="book.id" v-for="(book, index) in bookData">
        <Book :="{ ...book }" :myIndex="index" :handleBookClick="handleBookClick" />
      </div>
    </div>
  </div>
</template>
