<template>
  <div class="hello">
    <h3>{{title}}</h3>
    <span class="p-float-label">
        <InputText id="username" type="text" v-model="value" />
        <label for="username">Username</label>
    </span>
    <Button label="Send" v-on:click="send" />
    <span>
        {{info}}
    </span>
  </div>
</template>

<script>
import InputText from 'primevue/inputtext'
import Button from 'primevue/button'
import axios from 'axios'

export default {
  name: 'Gitops',
  data () {
    return {
      value: '',
      info: '',
      title: process.env.TITLE_APP
    }
  },
  components: {
    InputText, Button
  },

  methods: {
    send: function (event) {
      axios
        .get(process.env.ROOT_API + this.value)
        .then(response => (this.info = response.data))
      console.log('test')
      console.log(this.info)
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
