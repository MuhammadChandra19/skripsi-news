<template>
  <div class="categories">
    <p 
      class="item"
      v-for="(category, idx) in list"
      :key="idx"
      @click="setCategory(category)"
    >
      {{ category }}
    </p>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'CategoryList',
  data() {
    return {
      list: [
        'general', 
        'entertainment', 
        'business', 
        'health', 
        'science', 
        'sports',
        'technology'
      ]
    }
  },
  methods: {
    setCategory(category: string): void {
      location.assign(`${location.origin}${location.pathname}?category=${category}`)
    }
  }
})
</script>
<style lang="scss">
.categories {
  background-color: #333;
  overflow: auto;
  white-space: nowrap;
  margin-left: auto;
  margin-right: auto;
  position: relative;
  z-index: 6;
  text-align: center;
}
.categories .item {
  margin-bottom: 0px;
  cursor: pointer;
  margin-left: 13px;
  display: inline-block;
  color: white;
  text-align: center;
  padding: 14px;
  text-decoration: none;
}
</style>
