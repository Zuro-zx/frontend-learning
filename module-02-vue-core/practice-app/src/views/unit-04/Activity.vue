<script setup>
import { ref, computed } from 'vue'

const activityList = ref([
  {
    title: '2026 春季校园歌手大赛',
    status: 'signing',
    cover: 'https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?w=320&h=180&fit=crop&q=80'
  },
  {
    title: '校园篮球联赛',
    status: 'draft',
    cover: 'https://images.unsplash.com/photo-1574623452334-1e0ac2b3ccb4?w=320&h=180&fit=crop&q=80'
  }
])

const currentIndex = ref(0)
const current = computed(() => activityList.value[currentIndex.value])

function next() {
  currentIndex.value = (currentIndex.value + 1) % activityList.value.length
}
function prev() {
  currentIndex.value = (currentIndex.value - 1 + activityList.value.length) % activityList.value.length
}
</script>

<template>
  <div class="card">
    <img :src="current.cover" :alt="current.title">
    <h3>{{ current.title }}</h3>

    <span class="tag" :class="{
      'tag-sign': current.status === 'signing',
      'tag-draft': current.status === 'draft'
    }">
      {{ current.status === 'signing' ? '报名中' : '草稿' }}
    </span>

    <br>
    <button :disabled="current.status !== 'draft'">下架</button>

    <div style="margin-top:15px">
      <button @click="prev">上一张</button>
      <button @click="next">下一张</button>
    </div>
  </div>
</template>

<style>
.card {
  width: 360px;
  border: 1px solid #eee;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 2px 6px #00000015;
  margin: 20px auto;
}

img {
  width: 320px;
  height: 180px;
  object-fit: cover;
  display: block;
  margin: 10px auto;
}

.tag {
  padding: 4px 8px;
  color: #fff;
  background: #409eff;
  border-radius: 4px;
}

.tag-sign {
  background: #5ca67b;
}
</style>