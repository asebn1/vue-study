<template>
  <!-- 최상위 div는 하나만 존재한다. -->
  <div>
    <app-header
      v-bind:propsdata="str" 
      v-on:renew="renewStr"
     ></app-header> 
  </div>
</template>

<script>
// 1. 들고오기
import AppHeader from './components/AppHeader.vue';

export default {
  // data: {}가 아니라 function으로 진행해야한다.
  data: function() {
    return {
      str: "Header"
    }
  },
  components: {
    'app-header': AppHeader // 2. 등록하기
  },
  methods: {
    renewStr: function(){
      this.str = 'hi'
    }
  }
}
</script>

<style>

</style>