<script setup>
import { defineProps } from "vue";

const { author, title, id, myIndex } = defineProps({
    author: String,
    title: String,
    id: Number,
    myIndex: Number,
    handleBookClick: Function
});
</script>

<template>
    <div >
        <div
            class="relative rounded-2xl max-w-[20rem] flex flex-col gap-1 text-center items-center text-white bg-white p-3 border-black border-4 border-solid">
            <p class="absolute top-0 left-0 bg-black pl-4 px-3 py-1 rounded-br-3xl rounded-tl-xl">
                # {{ myIndex + 1 }}
            </p>
            <div class="w-full rounded-t-xl h-full overflow-hidden flex flex-col items-center bg-blue-600 p-1">
                <img class="object-cover rounded-lg" src="../images/book-img.png" alt="the book image" />
            </div>
            <h1 class="bg-blue-600 font-bold text-lg w-full p-2">{{ author }}</h1>
            <h4 class="bg-blue-600 w-full rounded-b-lg p-2">{{ title }}</h4>
            <button class="bg-blue-600 w-full rounded-lg shadow-black shadow-lg hover:bg-blue-900 active:scale-105" @click="()=> handleBookClick(id)" >Click Me</button>
        </div>
    </div>
</template>
