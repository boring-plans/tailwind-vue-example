<script setup>
import Card from './components/CommentCard.vue'
import {comments} from './components/comments'
</script>

<template>
  <div class="bg-sky-100 w-full min-h-[100vh] p-4 columns-1 sm:columns-2 md:columns-3 lg:columns-4">
    <Card 
      v-for="comment, index in comments"
      :key="index"
      :content="comment.content" 
      :nickname="comment.user.nickname" 
      :postTime="comment.timeStr" 
      :likes="comment.likedCount"
      :avatar="comment.user.avatarUrl"
      />
  </div>
</template>
