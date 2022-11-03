<script setup>
import { ref } from 'vue'

defineProps({
  content: String,
  nickname: String,
  avatar: String,
  likes: Number,
  postTime: String
})
</script>

<template>
  <div class="break-inside-avoid mb-4 flex flex-col p-4 bg-violet-300 rounded-xl hover:shadow-[0_0_5px_5px_rgba(220,210,260,62)]">
    <div class="flex items-center text-lg text-slate-500">
      <img :src="avatar" 
        class="w-[24px] h-[24px] rounded-xl" />
      <div class="ml-4">{{nickname}}</div>
    </div>
    <div class="text-xl font-bold text-slate-500 my-4">"{{content}}"</div>
    <div class="text-sm flex justify-between items-center">
      <div class="text-pink-500">&hearts; {{likes}}</div>
      
      <div class="italic text-xs">On {{postTime}}</div>
    </div>
  </div>
</template>
