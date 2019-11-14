<template>
  <div id="app">
    <div class="card">
      <p>What's your New Year wishes?</p>
      <div class="search_bx">
        <input type="text" @focus="checkTyping" @blur="checkTyping">
      </div>
      <div class="input_bx" v-if="startTyping">
        <textarea name="" id="" cols="80" rows="10"></textarea>
        <button type="button">submit</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      startTyping : false
    }
  },
  methods : {
    checkTyping : function(){
      if(this.startTyping){
        this.startTyping = false
      } else{
        this.startTyping = true
      }
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
