<template>
  <div id="login">
      <form action="login.vue">
        <p>登录到您的账户</p>
        <input type="text" v-model="username">
        <input type="text" v-model="password">
        <input type="submit">
      </form>
  </div>
</template>

<script>

  export default{

    data(){
      return{
      username:"",
      password:"",
      }
    },
    methods:{

      login:function () {
        this.axios.post('/user', {
          firstName: 'Fred',
          lastName: 'Flintstone'
        })
          .then(function (response) {
            console.log(response);
          })
          .catch(function (error) {
            console.log(error);
          });
      }

    }
  }

</script>
<style scoped>

  @import "./../../../static/Style/login.css";

</style>
