<template>
  <div class="row">
    <div v-for="item in list" :key="item.id" class="col-4">
      <div class="card h-100 shadow-sm">     
        <div class="card-body text-center">
          <img :src="item.avatar" :alt="item.title" class="card-img-top">
          <h5 class="card-title">{{ item.title }}</h5>
          <p class="card-text">{{ item.desc }}</p>
          <a href="" class="btn btn-primary">进入专栏</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang='ts'>
import{ defineComponent, PropType } from 'vue'
export interface ColumnPorps {
  id: number;
  title: string;
  avatar?: string;
  desc: string;
}
export default defineComponent({
  name : 'ColumnList',
  props: {
    list: {
      type: Array as PropType<Array<ColumnPorps>>,
      required: true,
      default: () => {
        return{
          id: 1,
          title: 'test',
          avatar: '2tt',
          desc: 'shswhshw'
        }
      }
    }
  },
  setup(props){
    
  }
})
</script>

<style>

</style>