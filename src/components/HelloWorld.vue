<template>
  <div class="CopClass">
    <el-button @click.native="login">默认按钮</el-button>
  </div>
</template>

<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      input: ''
    }
  },
  methods: {
    login(){
      this.$axios.get('test/sout', {
      })
        .then(resp => {
          console.log(resp.data);
        }).catch(err => {
        console.log(err);
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
