<template>
  <q-page class="flex flex-center">
  <button @click="message=''">clear </button>
  <input v-model="message" @keyup="handleKeyup"/>
    <H5> {{message}}</H5>
  </q-page>
</template>

<script>
export default {
data() {
return {
  message: 'Test Vue'
}
},
methods: {
  clearMessage(){ 
    this.message =''
},
  handleKeyup(e){
    if(e.keyCode==27){
      this.message='ESC'
  } else if(e.keyCode==13){
      this.message='ENTER'
  }
}
}
}
</script>
