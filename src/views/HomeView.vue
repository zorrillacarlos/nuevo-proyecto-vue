<template>
    <div class="home">
    <h1>This is an Home page {{ msg }}</h1>
    <button class="btn btn-warning" @click="btnClick()">HAZ CLICK</button>
  </div>
</template>

<script>
export default {
  setup(){
    const btnClick = () => {
      console.log('Hola mundo')
    }
    let msg = 'Que hay de nuevo'
    return{
      btnClick,
      msg
    }
  }
}
</script>

<style>

</style>