<template>


  <div>
      <h4>Calculator With Vue</h4>
      <input type="number" v-model.number="FN"><br><br>
      <select v-model="symbol">
             <option>+</option>
             <option>-</option>
             <option>*</option>
             <option>/</option>
      </select><br><br>
      <input type="number" v-model.number="SN"><br><br>
      <span>---------------------------------</span><br><br>
      <span>The answer is  =      {{Calculate}}</span>

  </div>
 
</template>


<script>
export default {
     data(){
        return{
          FN:"",
          SN:"",
          symbol:"",
        }


     },
     computed:{
           Calculate(){
               if(this.symbol === "+"){
                 return this.FN+this.SN;

               }else if(this.symbol === "-"){
                 return this.FN-this.SN;

               }else if(this.symbol === "*"){
                 return this.FN*this.SN;

               }else if(this.symbol === "/"){
                 return this.FN/this.SN;
               }
              }
     },
}
</script>



<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
