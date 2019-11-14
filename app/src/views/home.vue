<template>
  <div class="wrap">
      <header class="header">头部哦</header>
      <main class="main">
          <div class="swp">我是swiper</div>
      </main>
  </div>
   
</template>
<script>
import axios from 'axios'
export default {
  data(){
    return {
   searchName:''
    }
  },

  methods:{
   search(){
     
   }
  },

  created(){
    axios.get('/api/use/getlist').then(res=>{
      console.log(res.data.sql)
    })
  }
}
</script>
<style scoped lang="">
.wrap{
    width:100%;
    height:100%;
    display: flex;
    flex-direction: column;
}
.header{
    width:100%;
    height:50px;
    border:1px solid #ccc;
}
.main{
    width:100%;
    height:600px;
    background:pink;
}
.swp{
    width:100%;
    height:140px;
    background:#ccc;
}
</style>
