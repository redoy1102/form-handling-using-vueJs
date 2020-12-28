<template>
  <div class="container" >
    <button style="margin-right: 10px" class="btn btn-primary" @click="componentToRender='compHome'" >Home</button>
    <button style="margin-right: 10px" class="btn btn-primary" @click="componentToRender='compAbout'" >About</button>
    <button style="margin-right: 10px" class="btn btn-primary" @click="componentToRender='compContact'" >Contact</button>

    <keep-alive>
      <component :is="componentToRender"></component>
    </keep-alive>

  </div>
</template>

<script>
import compAbout from './Components/About/About'
import compContact from './Components/Contact/Contact'
import compHome from './Components/Home/Home'
export default {
  data(){
    return{
      componentToRender: 'compHome'
    }
  },
  components: {
    compAbout,
    compContact,
    compHome,
  }
}
</script>