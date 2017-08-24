<!-- https://github.com/npm/npm/issues/13461 -->
<template>
  <div id="app">
    <!-- <div class="acoder codeMonkey" id="codeMonkey" v-on:click="letCode">
      <p>{{codeMonkeySay}}</p>
      <input id="codeMonkeyDo" type="text" v-model="codeMonkeyDoSth"/>
    </div>
    <div class="acoder codeGirl" id="codeGirl" v-on:click="letCode">
      <p>{{codeGirlSay}}</p>
      <input id="codeGirlDo" type="text" v-model="codeGirlDoSth"/>
    </div> -->
    <!-- *********************** -->
    <child-Component coder-id="codeMonkey" coder-say="Hi 我是程序猿"></child-Component>
    <child-Component coder-id="codeGirl" coder-say="Hi 我是程序媛"></child-Component>
  </div>
</template>

<script>
import childComponent from './components/childComponent.vue'
export default {
  name: 'app',
  components: {
    childComponent
  }/*,
  //// 复用组件时注释
  data:()=>{
    return {
      codeMonkeySay: 'Hi 我是程序猿',
      codeGirlSay: 'Hi 我是程序媛',
      codeMonkeyDoSth: '',
      codeGirlDoSth: ''
    }
  },
  methods:{
    letCode: function(event){
      let selectId = event.target.id;
      if(selectId === 'codeMonkey'){
        alert('coding ruby...');
        this.codeMonkeyDoSth = 'finish coding ruby!';

      }else if(selectId === 'codeGirl'){
        alert('coding javascript...');
        this.codeGirlDoSth = 'finish coding javascript!';
      }
      
    }

    // letCode: (event) => {
    //   console.log(this)
    //   let vm = this;
    //   if(event.target.id === 'codeMonkey'){
    //     alert('coding ruby...');
    //     vm.codeMonkeyDoSth = 'finish coding ruby!';

    //   }else if(event.target.id === 'codeGirl'){
    //     alert('coding javascript...');
    //     vm.codeGirlDoSth = 'finish coding javascript';
    //   }
      
    // }
    
  }*/
}
</script>

<style>
/*#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
.acoder{
  height: 100px;
  width: 700px;
  border: solid 1px;
}
.codeMonkey{
  border-color: blue
}
.codeGirl{
  border-color: pink
}
div{
  margin: 5px;
}
</style>
