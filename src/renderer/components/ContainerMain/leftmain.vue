<template>
  <div class="leftmain"  v-bind:style="stylengt">
    <left-navt></left-navt>
</div>
</template>
<script>
import Leftnavt from '@/components/ContainerMain/leftmeun/leftnavt'
export default {
  data() {
    return {
      stylengt: {
        height: "539px"
      }
    };
  },
  components: {
    'left-navt':Leftnavt
  },
  created() {
   
  },
  updated:function(){
    
  
  },
  methods: {
    
  },
  mounted () {
    this.stylengt.height = `${document.documentElement.clientHeight-61}px`;
    // 然后监听window的resize事件．在浏览器窗口变化时再设置下背景图高度．
    const that = this;
    window.onresize = function temp1() {
    that.stylengt.height = `${document.documentElement.clientHeight-61}px`;
    };
    
  }
};
</script>
<style scoped>
.leftmain {
  position: fixed;
  left: 0;
  top: 61px;
  width: 20%;
  bottom: 0;
  overflow-x: hidden;
  border-right: 1px solid #f1f1f1;
  /* border-top-right-radius: 10px; */
}
</style>
