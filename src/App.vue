<template>
  <div class="container">
    <category-list />
    <!-- <news /> -->
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import CategoryList from './CategoryList.vue'
// import News from 'vuemicro/News'
export default defineComponent({
  components: {
    CategoryList,
    // News
  }
})

</script>
<style lang="scss">
  .container {
    box-sizing: border-box;
    max-width: 500px;
    margin-left: auto;
    margin-right: auto;
    height: 100vh;
    overflow: scroll;
    -webkit-box-shadow: 4px 10px 16px -5px rgba(0,0,0,0.75);
    -moz-box-shadow: 4px 10px 16px -5px rgba(0,0,0,0.75);
    box-shadow: 4px 10px 16px -5px rgba(0,0,0,0.75);
  }
</style>
