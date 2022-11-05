<template>
    <p v-if="age > 25" >{{message}}</p>
    <p v-else>Your Age must be greater than 25 in order to View the message</p>
</template>

<script>
export default {
  name:'Greeting',
  props:['age'],
  data(){
    return{
      message : "Hello World !!",
    }
  }
}
</script>

<style scoped lang="scss">
h1:hover{
    color: darken($color: purple, $amount: 2%);
}
</style>