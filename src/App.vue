<template>
<div id="app" class="container">
  <ColumnList :list="list"></ColumnList>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ColumnList, { ColumnPorps } from './components/ColumnList.vue'

const testData: Array<ColumnPorps> = [
   {
    id: 1,
    title: 'hello',
    avatar: 'sgs',
    desc: 'sgs' 
  },
  {
    id: 2,
    title: 'world',
    avatar: 'sghs',
    desc: 'shswh' 
  },
  {
    id: 2,
    title: 'shshssgww',
    // avatar: 'sghs',
    desc: 'shswh' 
  },
  {
    id: 2,
    title: 'world',
    avatar: 'sghs',
    desc: 'shswh' 
  }
]
 
export default defineComponent({
  name: 'App',
  components: {
    ColumnList
  },
  setup(){
    return {
      list: testData
    }
  }
});
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
