<template>
	<div class="childComponent">
		<div v-bind:class="'acoder '+coderId" v-bind:id="coderId" v-on:click="letCode">
	      <p>{{coderSay}}</p>
	      <input id="codeMonkeyDo" type="text" v-model="coderDoSth"/>
	    </div>
	</div>
</template>
<script>
export default {
  name: 'app',
  data(){
    return {
      coderDoSth: ''
    }
  },
  props: ['coderId','coderSay'],
  methods:{
    letCode: function(event){
      if(event.target.id === 'codeMonkey'){
        alert('coding ruby...');
        this.coderDoSth = 'finish coding ruby!';

      }else if(event.target.id === 'codeGirl'){
        alert('coding javascript...');
        this.coderDoSth = 'finish coding javascript!';
      }
    }
  }
}
</script>