<template>
  <div class="about">
    <div>
      <button @click="openWindow">Open me</button>
      <button @click="closeWindow">Close me</button>
      <a href="#" onclick="javascript:window.close();opener.window.focus();" >Close Window</a>
    </div>
  </div>
</template>

<script>
export default {
  data()
  {
    return{
      url:'https://hemis.nammti.uz/oauth/authorize?response_type=code&client_id=3&redirect_uri=https%3A%2F%2Fosiyohometex.uz%2F',
      result:'',
    }
  },
  methods:{
    openWindow(){

      window.open(this.url,)
    },
    closeWindow(){
      window.open('','_parent','');
      window.close();
    }
  }
}
</script>
