<script setup>
import Receipt from "@/components/Receipt.vue"
import {ref} from 'vue'
const count = ref(0)
let receiptName = []
let receiptData = ["", "", "", ""]

const posts = ref([
  { name: "name", ingredients: "ingredients", time: "kjdfsguzkf", desc: "dkjsugfkuesfgsu" }
])


console.log(count)
</script>

<template>
  <main>
    <span class="text-5xl text-center">Recipe Book</span>
    <div class="text-center my-8">
      <Receipt
      v-for="post in posts"
      :name="post.name"
      :ingredients="post.ingredients"
      :time="post.time"
      :desc="post.desc"/>
      <button @click="count++">Create new receipt {{count}}</button>
    </div>
    
    <div class="text-center">
        <div class="flex flex-col gap-1 border-none no-underline">

            <span>Name: {{ name }} </span>
            <input type="text" v-model="name" class="">
            <span>Ingredients: {{ ingredients }} </span>
            <input type="text" v-model="ingredients">
            <span>Required time: {{ time }}</span>
            <input type="text" v-model="time">
            <span>Description: {{ desc }}</span>
            
            <input type="text" v-model="desc">
        </div>
        <button >Add recipe</button>
      </div>
      
  </main>
</template>
